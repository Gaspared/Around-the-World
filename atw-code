use_bpm 122

live_loop :ATW do
  
  live_loop :bass do
    use_synth :saw
    
    16.times do
      baseline1
    end
    
    14.times do
      baseline2
    end
    
    16.times do
      baseline3
    end
    
    stop
  end
  
  live_loop :drums do
    
    32.times do
      drumline1
    end
    
    32.times do
      drumline2
    end
    
    48.times do
      drumline3
    end
    
    32.times do
      drumline4
    end
    
    56.times do
      drumline2
    end
    
    stop
  end
  
  live_loop :synthesizer do
    
    use_synth :tb303
    16.times do
      synthesizer1
    end
    
    use_synth :chiplead
    live_loop :wah, delay: 32 do
      80.times do
        synthesizer3
      end
      stop
    end
    
    use_synth :tb303
    8.times do
      synthesizer2
    end
    
    sleep 96
    8.times do
      synthesizer2
    end
    
    stop
  end
    
  stop
end

define :baseline1 do
  with_fx :ixi_techno, mix: 0.2 do
    with_fx :lpf, cutoff: 50 + tick * 3 do
      play_pattern_timed [:fs2, :e2, :d2, :c2, :b1, :a1, :g1, :g1, :a1],
        [ 0.5, 0.5, 0.5, 0.5, 0.5, 0.5, 0.5, 0.25, 0.25],
        release: 0.0, sustain: 0.125, amp: 2
    end
  end
end

define :baseline2 do
  with_fx :lpf, cutoff: 80 do
    play_pattern_timed [:a1, :a1, :a1, :a1, :b1, :c2, :r, :c2, :c2, :c2, :d2, :e2, :r, :e2, :e2, :e2, :fs2, :e2, :d2, :c2, :b1, :a1, :g1, :g1, :a1],
      [1, 1, 1, 0.5, 0.25, 0.25, 1, 1, 1, 0.5, 0.25, 0.25, 1, 1, 1, 1, 0.5, 0.5, 0.5, 0.5, 0.5, 0.5, 0.5, 0.25, 0.25],
      release: 0.0, sustain: 0.3
  end
end

define :baseline3 do
  with_fx :lpf, cutoff: 80 do
    play_pattern_timed [:e2, :d3, :e3, :e2, :d3, :e2, :d3, :e2, :d3, :e3, :c2, :c3, :c2, :c3, :c2, :b1, :b1, :a2, :b2, :g2],
      [0.5, 0.5, 0.5, 0.5, 0.5, 0.25, 0.5, 0.25, 0.25, 0.25, 0.5, 0.5, 0.25, 0.25, 0.5, 0.25, 0.5, 0.25, 0.5, 0.5],
      release: 0.0, sustain: 0.3
  end
end

define :synthesizer1 do
  with_fx :ixi_techno, mix: 0.4 do
    with_fx :lpf, cutoff: 50 + tick * 3  do
      play_pattern_timed [:e4, :d4, :a3, :a3, :a3, :g3], [0.5, 1, 1, 1, 0.25, 0.25],
        attack: 0.0, sustain: 0.05, release: 0.1, res: 0.3
    end
  end
end

define :synthesizer2 do
  with_fx :rhpf, res: 0.8, cutoff: 65  do
    with_fx :echo, mix: 0.2, decay: 0.5 do
      play_pattern_timed [nil, :a3, :a3, :d4 , :c4, :a3, :a3, :g3, :b3, :e3, :e3, :e4, :d4, :b3, :a3, :g3, :g3, :a3, :e3],
        [3.5, 0.25, 0.25, 0.5, 1, 1, 1, 0.25, 3.75 , 0.25, 0.25, 0.5, 0.5, 0.5, 0.5, 1, 0.5, 0.25, 0.25 ],
        attack: 0.0, sustain: 0.03, release: 0.1, res: 0.8, amp: 0.6
    end
  end
end

define :synthesizer3 do
  with_fx :ixi_techno, mix: 1, phase: 2 do
    play_pattern_timed [:e3, :g3, :b2, :d3, :d3], [0.5, 1, 0.5, 1.75, 0.25],
      attack: 0.0, sustain: 0.05, release: 0.1, width: 0, amp: 0.7
  end
end

define :drumline1 do
  with_fx :lpf, cutoff: 60 + tick * 2 do
    sample :bd_fat, amp: 2
    sleep 1
    sample :bd_fat, amp: 2
    sample :sn_zome, amp: 0.7
    sleep 1
  end
end

define :drumline2 do
  sample :bd_fat, amp: 3
  sleep 0.5
  sample :drum_cymbal_closed, amp: 0.7
  sleep 0.5
  sample :bd_fat, amp: 3
  sample :sn_zome, amp: 0.7
  sleep 0.5
  sample :drum_cymbal_closed, amp: 0.7
  sleep 0.5
end

define :drumline3 do
  sample :bd_fat, amp: 3
  sleep 0.5
  sample :drum_cymbal_closed, amp: 0.4
  sleep 0.5
  sample :bd_fat, amp: 3
  sample :sn_zome, amp: 0.7
  sleep 0.5
  sample :drum_cymbal_closed, amp: 0.4
  sleep 0.5
end

define :drumline4 do
  sample :bd_fat, amp: 3
  sleep 0.5
  sleep 0.5
  sample :bd_fat, amp: 3
  sample :sn_zome, amp: 0.7
  sleep 0.5
  sleep 0.5
end
