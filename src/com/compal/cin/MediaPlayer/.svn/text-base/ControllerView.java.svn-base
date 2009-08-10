
package com.compal.cin.MediaPlayer;

import android.app.Activity;

import android.content.Intent;

import android.os.Bundle;
import android.util.Log;


import android.widget.MediaController;

import android.widget.VideoView;


/**
 * 09-2-04 by Hang Lu:
 * + function: Video play back controlled by space bar
 */
public class ControllerView extends Activity 
 {

    private VideoView videoView;
    
    private static final String TAG = Debug.TAG;
   
    /**
     * Called when the activity is first created.
     */
    public void onCreate(Bundle icicle) {
        super.onCreate(icicle);
        setContentView(R.layout.controller_view);

        videoView = (VideoView)findViewById(R.id.controller_view);
        Intent i = getIntent();
        
        /**
         * Retrieve path from Intent
         */
        
        String path = i.getData().getPath();
  	    Log.v(TAG, "Controller: I will play: " + path);
        
  	    videoView.setVideoPath(path);

     	videoView.setMediaController(new MediaController(this, true));   
     	
     	videoView.start();  
     	
     	videoView.measure(100, 100);
    }
}
