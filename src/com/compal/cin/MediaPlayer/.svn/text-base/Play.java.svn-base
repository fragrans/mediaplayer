/**
 * Play.java serves as a unique interface to source media
 * Detailed info will be deferred to later update.
 */
package com.compal.cin.MediaPlayer;

import android.app.Activity;
import android.content.Intent;
import android.util.Log;

/**
 * @author cocos
 * 
 */
public class Play {
	Activity ctx;
	static String TAG = Debug.TAG;

	public Play(Activity ctx) {
		this.ctx = ctx;
	}

	public void play(String path) {
		Intent i = new Intent();

		/**
		 * video absolute path will pass to new view
		 */
		i.putExtra("path", path);


		Long flag = 0L;
		Log.v(TAG, "Item: " + flag.toString());
		if (flag == 0) {
			i.setClass(ctx, ControllerView.class);
		} else {
			i.setClass(ctx, SurfaceViewView.class);
			
		}
		ctx.startActivity(i);
	}

}
