audio ��ǩ
=======

`<audio>` Ԫ��������ҳ���������Ƶ��

	<audio src="music.mp3" controls="controls"></audio>
	
Ҳ����ͨ���� `<audio>` Ԫ����Ƕ��һ������ `<source>` Ԫ�أ���ָ�������ļ���ʹ�ø÷���ʱ��`<audio>` Ԫ�ص� `src` ���Ա����ԡ�����֤ʵ��

	<audio controls="controls">
		<source src="music.mp3" type="audio/mp3" />
		<source src="music.ogg" type="audio/ogg" />
	</audio>

����
----

###1.autoplay

ָ����Ƶ��ҳ�������ɺ��Զ���ʼ���š�

����ֵ��
>1. autoplay

###2.controls

ָ����ʾ���ſؼ���һ���������/��ͣ��ť��������������ʱ�䡢�������ڻ���ȿؼ���

����ֵ��
>1. controls

###3.loop

ָ����Ƶѭ�����š�

����ֵ��
>1. loop

###4.preload

ָ����ҳ�������ɺ����������Ƶ�ļ������Ѿ�ָ�� `autoplay`������Ա����ԡ�

����ֵ��
>1. auto ����ȫ������
>2. metadata ������Ԫ���ݣ���Ƶ��Ϣ��
>3. none ������

###5.src

ָ����Ƶ�ļ���URL��

Audio����
----------

�ο���[HTMLMediaElement](https://developer.mozilla.org/zh-CN/docs/DOM/HTMLMediaElement "HTMLMediaElement")

###����

1.src

��¼����Ƶ�ļ���URL��

	var src=audio.src; // ��ȡURL
	audio.src="music.mp3"; // �޸�URL

2.currentTime

��¼�˵�ǰ����ʱ�䣨��λ���룩��

	var time=audio.currentTime; // ��ȡ��ǰʱ��
	audio.currentTime=30; // ���õ�ǰʱ��Ϊ30��

3.volume

��¼����Ƶ����������Χ��0.0-1.0����

	var volume=audio.volume; // ��ȡ����
	audio.volume+=0.1; // ��������
	


###����

1.play()

��ʼ���š�

	audio.play(); // ��ʼ����

2.pause()

��ͣ���š�

	audio.pause(); // ��ͣ����