package com.compal.cin.MediaPlayer;

import java.io.IOException;

import android.app.Activity;

import android.media.MediaRecorder;

import android.os.Bundle;

import android.view.View;
import android.widget.Button;


public class AudioRecord extends Activity {
	private static final String TAG = Debug.TAG;

	MediaRecorder recorder;
	/**
     * Called when the activity is first created.
     */
    public void onCreate(Bundle icicle) {
        super.onCreate(icicle);
        setContentView(R.layout.audio_record);
        Button button = (Button)this.findViewById(R.id.button_start);
        button.setOnClickListener(new Button.OnClickListener() {
            public void onClick(View v) {
                // Perform action on click
            	recorder = new MediaRecorder();

            	recorder.setAudioSource(MediaRecorder.AudioSource.MIC);
        	    recorder.setOutputFormat(MediaRecorder.OutputFormat.THREE_GPP);
        	    recorder.setAudioEncoder(MediaRecorder.AudioEncoder.AMR_NB);
        	    recorder.setOutputFile("/sdcard/test.3gp");
        	    
        	    try {
					recorder.prepare();
				} catch (IllegalStateException e) {
					// TODO Auto-generated catch block
					e.printStackTrace();
				} catch (IOException e) {
					// TODO Auto-generated catch block
					e.printStackTrace();
				}
        	    recorder.start();

            }
        });

        button = (Button)this.findViewById(R.id.button_stop);
        button.setOnClickListener(new Button.OnClickListener() {
            public void onClick(View v) {
                // Perform action on click
            	recorder.stop();
            	recorder.release();
            }
        });
    }
}
