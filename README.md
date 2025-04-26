# ece463-563-project-1-cache-design-memory-hierarchy-design-version-1-0-solved
**TO GET THIS SOLUTION VISIT:** [ECE463-563  Project #1: Cache Design, Memory Hierarchy Design (Version 1.0) Solved](https://www.ankitcodinghub.com/product/ece463-563-project-1-cache-design-memory-hierarchy-design-version-1-0-solved-2/)


---

📩 **If you need this solution or have special requests:** **Email:** ankitcoding@gmail.com  
📱 **WhatsApp:** +1 419 877 7882  
📄 **Get a quote instantly using this form:** [Ask Homework Questions](https://www.ankitcodinghub.com/services/ask-homework-questions/)

*We deliver fast, professional, and affordable academic help.*

---

<h2>Description</h2>



<div class="kk-star-ratings kksr-auto kksr-align-center kksr-valign-top" data-payload="{&quot;align&quot;:&quot;center&quot;,&quot;id&quot;:&quot;125971&quot;,&quot;slug&quot;:&quot;default&quot;,&quot;valign&quot;:&quot;top&quot;,&quot;ignore&quot;:&quot;&quot;,&quot;reference&quot;:&quot;auto&quot;,&quot;class&quot;:&quot;&quot;,&quot;count&quot;:&quot;5&quot;,&quot;legendonly&quot;:&quot;&quot;,&quot;readonly&quot;:&quot;&quot;,&quot;score&quot;:&quot;5&quot;,&quot;starsonly&quot;:&quot;&quot;,&quot;best&quot;:&quot;5&quot;,&quot;gap&quot;:&quot;4&quot;,&quot;greet&quot;:&quot;Rate this product&quot;,&quot;legend&quot;:&quot;5\/5 - (5 votes)&quot;,&quot;size&quot;:&quot;24&quot;,&quot;title&quot;:&quot;ECE463-563&nbsp;  Project #1: Cache Design, Memory Hierarchy Design (Version 1.0) Solved&quot;,&quot;width&quot;:&quot;138&quot;,&quot;_legend&quot;:&quot;{score}\/{best} - ({count} {votes})&quot;,&quot;font_factor&quot;:&quot;1.25&quot;}">

<div class="kksr-stars">

<div class="kksr-stars-inactive">
            <div class="kksr-star" data-star="1" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="2" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="3" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="4" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="5" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>

<div class="kksr-stars-active" style="width: 138px;">
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>
</div>


<div class="kksr-legend" style="font-size: 19.2px;">
            5/5 - (5 votes)    </div>
    </div>
<h2>1.3.&nbsp; Programming languages for this project</h2>
You must implement your project using the C, C++, or Java languages, for two reasons. First, these languages are preferred for computer architecture performance modeling. Second, our Gradescope autograder only supports compilation of these languages.

<h1>2. Project Description</h1>
In this project, you will implement a flexible cache and memory hierarchy simulator and use it to compare the performance, area, and energy of different memory hierarchy configurations, using a subset of the SPEC 2006 benchmark suite, SPEC 2017 benchmark suite, and/or microbenchmarks.

<h1>3. Specification of Memory Hierarchy</h1>
Design a generic cache module that can be used at any level in a memory hierarchy. For example, this cache module can be “instantiated” as an L1 cache, an L2 cache, an L3 cache, and so on. Since it can be used at any level of the memory hierarchy, it will be referred to generically as CACHE throughout this specification.

<h2>3.1. Configurable parameters</h2>
CACHE should be configurable in terms of supporting any cache size, associativity, and block size, specified at the beginning of simulation:

<ul>
<li>SIZE: Total bytes of data storage.</li>
<li>ASSOC: The associativity of the cache. (ASSOC = 1 is a direct-mapped cache. ASSOC</li>
</ul>
= # blocks in the cache = SIZE/BLOCKSIZE is a fully-associative cache.) o BLOCKSIZE: The number of bytes in a block.

&nbsp;

There are a few constraints on the above parameters: 1) BLOCKSIZE is a power of two and 2) the number of <em>sets</em> is a power of two. <em>Note that ASSOC (and, therefore, SIZE) need not be a power of two</em>. As you know, the number of sets is determined by the following equation:

#<em>sets </em>= <em>SIZE&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; </em>

<em>ASSOC</em><sub>× </sub><em>BLOCKSIZE </em><strong><em>3.2. Replacement policy </em></strong>

CACHE should use the LRU (least-recently-used) replacement policy.

<h2>3.3. Write policy</h2>
CACHE should use the WBWA (write-back + write-allocate) write policy.

o Write-allocate: A write that misses in CACHE will cause a block to be allocated in CACHE. Therefore, both write misses and read misses cause blocks to be allocated in CACHE. o Write-back: A write updates the corresponding block in CACHE, making the block dirty. It does not update the next level in the memory hierarchy (next level of cache or memory). If a dirty block is evicted from CACHE, a writeback (<em>i.e.</em>, a write of the entire block) will be sent to the next level in the memory hierarchy.

<h2>3.4. Allocating a block: Sending requests to next level in the memory hierarchy</h2>
Your simulator must be capable of modeling one or more instances of CACHE to form an overall memory hierarchy, as shown in Figure 1.

&nbsp;

CACHE receives a read or write request from whatever is above it in the memory hierarchy (either the CPU or another cache). The only situation where CACHE must interact with the next level below it (either another CACHE or main memory) is when the read or write request misses in CACHE. When the read or write request misses in CACHE, CACHE must “allocate” the requested block so that the read or write can be performed.

&nbsp;

Thus, let us think in terms of allocating a requested block X in CACHE. The allocation of requested block X is actually a two-step process. <em>The two steps must be performed in the following order</em>.

<ol>
<li><em>Make space for the requested block X</em>. If there is at least one invalid block in the set, then there is already space for the requested block X and no further action is required (go to step 2). On the other hand, if all blocks in the set are valid, then a victim block V must be singled out for eviction, according to the replacement policy (Section 3.2). If this victim block V is dirty, then a write of the victim block V must be issued to the next level of the memory hierarchy.</li>
<li><em>Bring in the requested block X</em>. Issue a read of the requested block X to the next level of the memory hierarchy and put the requested block X in the appropriate place in the set (as per step 1).</li>
</ol>
&nbsp;

To summarize, when allocating a block, CACHE issues a write request (<em>only</em> if there is a victim block and it is dirty) followed by a read request, both to the next level of the memory hierarchy. Note that each of these two requests could themselves miss in the next level of the memory hierarchy (if the next level is another CACHE), causing a cascade of requests in subsequent levels. <em>Fortunately, you only need to correctly implement the two steps for an allocation locally within CACHE. If an allocation is correctly implemented locally (steps 1 and 2, above), the memory hierarchy as a whole will automatically handle cascaded requests globally. </em>

<h2>3.5. Updating state</h2>
After servicing a read or write request, whether the corresponding block was in the cache already (hit) or had just been allocated (miss), remember to update other state. This state includes LRU counters affiliated with the set as well as the valid and dirty bits affiliated with the requested block.

&nbsp;

<strong>Figure 1.&nbsp; Your simulator must be capable of modeling one or more instances of CACHE to form an overall memory hierarchy.</strong>

<ol start="4">
<li><strong> ECE 563 Students: Augment CACHE with Stream-Buffer </strong></li>
</ol>
<h1>Prefetching</h1>
Students enrolled in ECE 563 must additionally augment CACHE with a prefetch unit. The prefetch unit implements Stream Buffers.

&nbsp;

In this project, consider the prefetch unit to be an extension implemented within CACHE. This preserves the clean abstraction of one or more instances of CACHE interacting in an overall memory hierarchy (see Figure 1), where each CACHE may have a prefetch unit within it.

<h2>4.1. CACHE should support a configurable prefetch unit</h2>
Your generic implementation of CACHE should support a configurable prefetch unit as follows. The prefetch unit has N Stream Buffers. Each Stream Buffer contains M memory blocks. Both N and M should be configurable. Setting N=0 disables the prefetch unit.

<h2>4.2. Operation of a single Stream Buffer</h2>
A Stream Buffer is a simple queue that is capable of holding M <em>consecutive</em> memory blocks.

&nbsp;

A Stream Buffer has a single valid bit that indicates the validity of the buffer as a whole. If its valid bit is 0, it means the Stream Buffer is empty and doesn’t contain a prefetch stream. If its valid bit is 1, it means the Stream Buffer is full and contains a prefetch stream (M consecutive memory blocks).

&nbsp;

When CACHE receives a read or write request for block X, both CACHE and its Stream Buffer are checked for a hit. Note that all Stream Buffer entries, not just the first entry (as in the original Stream Buffer paper), are searched for block X. There are four possible scenarios:

&nbsp;

<ol>
<li><strong>Scenario #1 (create a new prefetch stream): Requested block X misses in CACHE and misses in Stream Buffer:</strong> Handle the miss in CACHE as usual (see Section 3.4). In addition to fetching the requested block X into CACHE, prefetch the next M consecutive memory blocks into the Stream Buffer. That is, prefetch memory blocks X+1, X+2, …, X+M into the Stream Buffer, thereby replacing the entire contents of the Stream Buffer. Note that prefetches are implemented by issuing read requests to the next level in the memory hierarchy.<a href="#_ftn1" name="_ftnref1"><sup>[1]</sup></a> Also note that replacing the contents of the Stream Buffer does not involve any writebacks from the Stream Buffer: this will be explained in Section 4.4.</li>
<li><strong>Scenario #2 (benefit from and continue a prefetch stream): Requested block X misses in CACHE and hits in the Stream Buffer:</strong> Perform an allocation in CACHE as follows. First, make space in CACHE for the requested block X (as described in Section 3.4). Second, instead of fetching the requested block X from the next level in the memory hierarchy, copy the requested block X from the Stream Buffer into CACHE (since the</li>
</ol>
&nbsp;

Stream Buffer contains the requested block X, in this scenario). Next, manage the Stream Buffer as illustrated in Figure 2. Notice in the “before” picture, the fourth entry of the Stream Buffer hit (it contained the requested block X). As shown in the “after” picture, all blocks before and including block X (X-3, X-2, X-1, X) are removed from the Stream Buffer, the blocks after block X (X+1, X+2) are “shifted up”, and the newly freed entries are refilled by prefetching the next consecutive blocks (issue prefetches of blocks X+3, X+4, X+5, X+6). A non-shifting circular buffer implementation, based on a head pointer that points to the least block address in the prefetch stream, is more efficient in real hardware <em>and</em> in software simulators, and is illustrated in Figure 3.

<ol start="3">
<li><strong>Scenario #3 (do nothing): Requested block X hits in CACHE and misses in the Stream Buffer:</strong> In this case, nothing happens with respect to the Stream Buffer.</li>
<li><strong>Scenario #4 (continue prefetch stream to stay in sync with demand stream): Requested block X hits in CACHE and hits in the Stream Buffer:</strong> Manage the Stream Buffer identically to Scenario #2. The only difference is that the requested block X hit in CACHE, so there is no transfer from Stream Buffer to CACHE.</li>
</ol>
&nbsp;

&nbsp;

<em>before </em>

<table width="233">
<tbody>
<tr>
<td width="56">X-3</td>
<td rowspan="6" width="121">&nbsp;</td>
<td width="56">X-3</td>
</tr>
<tr>
<td width="56">X-2</td>
<td width="56">X-2</td>
</tr>
<tr>
<td width="56">X-1</td>
<td width="56">X-1</td>
</tr>
<tr>
<td width="56">X</td>
<td width="56"></td>
</tr>
<tr>
<td width="56">X+1</td>
<td width="56">X+1</td>
</tr>
<tr>
<td width="56">X+2</td>
<td width="56">X+2</td>
</tr>
</tbody>
</table>
<h1>V (valid) = 1</h1>
&nbsp;

<em>after</em>

<table width="56">
<tbody>
<tr>
<td width="56">X+1</td>
</tr>
<tr>
<td width="56">X+2</td>
</tr>
<tr>
<td width="56">&nbsp;</td>
</tr>
<tr>
<td width="56">&nbsp;</td>
</tr>
<tr>
<td width="56">&nbsp;</td>
</tr>
<tr>
<td width="56">&nbsp;</td>
</tr>
</tbody>
</table>
V (valid) = 1

X+1 X+2 X+3 hit X+4 X+5

<h1>X+6</h1>
&nbsp;

<strong>Figure 2.&nbsp; Managing the Stream Buffer when there is a hit in the Stream Buffer (scenarios #2 and #4). </strong>

&nbsp;

<em>before &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; after</em>

<table width="233">
<tbody>
<tr>
<td width="56">&nbsp;X-3</td>
<td rowspan="5" width="121">head à</td>
<td width="56">X-3</td>
</tr>
<tr>
<td width="56">X-2</td>
<td width="56">X-2</td>
</tr>
<tr>
<td width="56">X-1</td>
<td width="56">X-1</td>
</tr>
<tr>
<td width="56">X</td>
<td width="56"></td>
</tr>
<tr>
<td width="56">X+1</td>
<td width="56">&nbsp;X+1</td>
</tr>
</tbody>
</table>
V (valid) = 1

head à

hit

X+1

X+2

&nbsp;

<strong>Figure 3.&nbsp; A non-shifting circular buffer implementation is more efficient in hardware <em>and</em> in software simulators. </strong>

<h2>4.3. Multiple Stream Buffers</h2>
The operation of a single Stream Buffer, described in the previous section, extends to multiple Stream Buffers. The main difference is that all Stream Buffers are checked for a hit.

&nbsp;

For Scenario #1 (request misses in CACHE and misses in all Stream Buffers), one of the Stream Buffers must be chosen for the new prefetch stream: select the least-recently-used Stream Buffer, <em>i.e.</em>, apply the LRU policy to the Stream Buffers as a whole. When a new stream is prefetched into a particular Stream Buffer (Scenario #1), or a particular Stream Buffer supplies a requested block to CACHE (Scenario #2), or we are keeping a Stream Buffer in sync (Scenario #4), that Stream Buffer becomes the most-recently-used buffer.

&nbsp;

<strong>Policy for multiple Stream Buffer hits: </strong>

&nbsp;

It is possible for two or more Stream Buffers to have some blocks in common (redundancy). For example, suppose all Stream Buffers are initially invalid and CACHE is empty; the CPU requests block X which creates the prefetch stream X+1 to X+6 in a first Stream Buffer (assume M=6); and then the CPU requests block X-2 which creates the prefetch stream X-1 to X+4 in a second Stream Buffer; thus, after these initial two misses, the Stream Buffers have X+1 to X+4 in common. Other scenarios create redundancy as well, such as one continuing prefetch stream reaching the start of another prefetch stream.

&nbsp;

Redundancy means that a given request may hit in multiple Stream Buffers. Managing multiple Stream Buffers as in Figure 2, for the same hit, results in redundant prefetches because the multiple Stream Buffers will all try to continue their overlapping streams. <strong>A simple solution is to only consider the hit to the most-recently-used Stream Buffer among those that hit and ignore the other hits.</strong> From a simulator standpoint, this could mean (for example) searching Stream Buffers for a hit in recency order, and stopping at the first hit. Only <em>that</em> Stream Buffer is managed as shown in Figure 2, <em>i.e.</em>, only <em>that</em> Stream Buffer continues its prefetch stream.

<h2>4.4. Assume Stream Buffers are updated by writebacks with no effect on recency (no explicit modeling required in your simulator)</h2>
A Stream Buffer never contains dirty blocks, that is, it never contains a block whose content differs from the same block in the next level of the memory hierarchy. The benefit of this design is that replacing the contents of the Stream Buffer will never require writebacks from the Stream Buffer.

&nbsp;

In this section, we discuss a Stream Buffer complication that we will handle <em>conceptually</em>. The problem and solution are only discussed out of academic interest. <strong>The solution does not require any explicit support in the simulator.</strong>

&nbsp;

Consider that a dirty copy of block Y may exist in CACHE while a clean copy of block Y exists in a Stream Buffer. Here is a simple example of how we can get into this situation (assume M=6 for the example):

<ul>
<li>Write request to block Y misses in CACHE. Block Y is allocated in CACHE, write is performed, and block Y is dirty in CACHE. Prefetch stream Y+1 to Y+6 is created in a first Stream Buffer, although this is not germane for this example.</li>
<li>Then, a request to block Y-2 misses in CACHE. Prefetch stream Y-1 to Y+4 is created in a second Stream Buffer. Thus, at this point, CACHE has a dirty copy of block Y and the second Stream Buffer has a clean copy of block Y.</li>
</ul>
Now, suppose CACHE evicts its dirty copy of block Y (<em>e.g.</em>, it is replaced by a missed block Z) before referencing it again (fyi: referencing it as a hit might wipe it from the Stream Buffer to keep the latter’s prefetch stream in sync with demand references, as per scenario #4). Stale block Y still exists in the Stream Buffer which could lead to incorrect operation in the future, namely, when the CPU requests block Y again and hits on the stale copy in the Stream Buffer.

&nbsp;

We will assume a solution that does NOT require any code in your simulator. When a dirty block Y is evicted from CACHE (<em>i.e.</em>, when there is a writeback), any Stream Buffers that contain block Y update their copy of block Y. In this way, a Stream Buffer’s copy of block Y will remain clean and up to date with respect to the next level, since the writeback is performed not only in the next level but also in the Stream Buffer. In addition, let us also assume that this operation does NOT update recency among Stream Buffers. Therefore, the only effect is updating data, and your simulator does not model data.

&nbsp;

<h2>5. Memory Hierarchies to be Explored in this Project</h2>
While Figure 1 illustrates an arbitrary memory hierarchy, you will only study the memory hierarchy configurations shown in Figure 4 (ECE 463) and Figure 5 (ECE 563). Also, these are the only configurations that Gradescope will test.

&nbsp;

For this project, all CACHEs in the memory hierarchy will have the same BLOCKSIZE.

&nbsp;

from CPU&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; from CPU

<strong>Figure 4.&nbsp; ECE 463: Two configurations to be studied. </strong>

from CPU&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; from CPU&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; from CPU&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; from CPU

Main Memory&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; Main Memory

<strong>Figure 5.&nbsp; ECE 563: Four configurations to be studied. </strong>

&nbsp;

<h2>6. Inputs to Simulator</h2>
<h3>6.1. Traces</h3>
The simulator reads a trace file in the following format:

&nbsp;

r|w &lt;hex address&gt; r|w &lt;hex address&gt; …

&nbsp;

“r” (read) indicates a load and “w” (write) indicates a store from the processor.

&nbsp;

Example:

&nbsp;

r ffe04540 r ffe04544 w 0eff2340 r ffe04548 …

&nbsp;

Traces are posted on the Moodle website.

&nbsp;

<strong><u>NOTE:</u> </strong>

All addresses are 32 bits. When expressed in hexadecimal format (hex), an address is 8 hex digits as shown in the example trace above. In the actual trace files, you may notice some addresses are comprised of fewer than 8 hex digits: this is because there are leading 0’s which are not explicitly shown. For example, an address “ffff” is really “0000ffff”, because all addresses are 32 bits, <em>i.e.</em>, 8 nibbles.

<h3>6.2. Command-line arguments to the simulator</h3>
The simulator executable built by your Makefile must be named “sim” (the Makefile is discussed in Section 8).

&nbsp;

Your simulator must accept exactly 8 command-line arguments in the following order:

sim&nbsp;&nbsp; &lt;<em>BLOCKSIZE</em>&gt;

&lt;<em>L1_SIZE</em>&gt;&nbsp; &lt;<em>L1_ASSOC</em>&gt;

&lt;<em>L2_SIZE</em>&gt;&nbsp; &lt;<em>L2_ASSOC</em>&gt;

&lt;<em>PREF_N</em>&gt;&nbsp; &lt;<em>PREF_M</em>&gt;

&lt;<em>trace_file</em>&gt;

&nbsp;

<ul>
<li><em>BLOCKSIZE</em>: Positive integer.&nbsp; Block size in bytes.&nbsp; (Same block size for all caches in the memory hierarchy.)</li>
<li><em>L1_SIZE</em>: Positive integer.&nbsp; L1 cache size in bytes.</li>
<li><em>L1_ASSOC</em>: Positive integer.&nbsp; L1 set-associativity (1 is direct-mapped, L1_SIZE/BLOCKSIZE is fully-associative).</li>
<li><em>L2_SIZE</em>: Positive integer.&nbsp; L2 cache size in bytes.&nbsp; <em>L2_SIZE</em> = 0 signifies that there is no L2 cache. o <em>L2_ASSOC</em>:&nbsp; Positive integer.&nbsp; L2 set-associativity (1 is direct-mapped, L2_SIZE/BLOCKSIZE is fully-associative).</li>
<li><em>PREF_N</em>: Positive integer.&nbsp; Number of Stream Buffers in the L1 prefetch unit (if there is no L2) or the L2 prefetch unit (if there is an L2).&nbsp; <em>PREF_N</em> = 0 disables the prefetch unit.</li>
<li><em>PREF_M</em>: Positive integer.&nbsp; Number of memory blocks in each Stream Buffer in the L1 prefetch unit (if there is no L2) or the L2 prefetch unit (if there is an L2). o <em>trace_file</em>:&nbsp; Character string.&nbsp; Full name of trace file including any extensions.</li>
</ul>
&nbsp;

Example:&nbsp; 8KB 4-way set-associative L1 cache with 32B block size, 256KB 8way set-associative L2 cache with 32B block size, L2 prefetch unit has 3 stream buffers with 10 blocks each, gcc trace:

sim&nbsp; 32&nbsp; 8192&nbsp; 4&nbsp; 262144&nbsp; 8&nbsp; 3&nbsp; 10&nbsp; gcc_trace.txt

&nbsp;

&nbsp;

Some additional points:

<ul>
<li>You may assume that only valid arguments will be applied to your simulator by Gradescope. Thus, while it is good practice for programmers to check arguments (<em>g.</em>, check that the specified trace file exists and can be opened; <em>e.g.</em>, check that SIZE, ASSOC, and BLOCKSIZE lead to a feasible cache; <em>e.g.</em>, check that the correct number of arguments are passed in), you are NOT required to do so.</li>
<li>Although ECE 463 students do not implement prefetching, they must still parse the prefetching-related arguments the same as ECE 563 students. ECE 463 students may assume that, for their projects, Gradescope will always specify “0 0” for arguments PREF_N and PREF_M.</li>
<li>ECE 563 students may notice that, for this project, there is only one pair of prefetcher configuration arguments (PREF_N, PREF_M) and that these are applied only to the last level of cache in the memory hierarchy. This is consistent with Figure 5.</li>
</ul>
&nbsp;

&nbsp;

<h2>7. Outputs from Simulator</h2>
Your simulator should output the following:

<u>(See Section 8 regarding the formatting of these outputs and validating your simulator.)</u>

&nbsp;

<ol>
<li>Memory hierarchy configuration and trace filename.</li>
<li>The final contents of all caches and their stream buffers (if applicable). <u>For cache contents,</u> <u>blocks within a set must be printed out from most-recently-used to least-recently-used. Omit (do</u> <u>not print) invalid blocks within a set, if there are any. If a given set has no valid blocks, omit (do</u> <u>not print) that set. Stream buffers (if present) must be printed out from most-recently-used to</u> <u>least-recently-used, and only valid stream buffers should be printed out.</u></li>
<li>The following measurements: (<em>note that “miss” means neither the cache nor its stream buffers </em></li>
</ol>
<em>hit</em>)

&nbsp;

<ol>
<li>number of L1 reads</li>
<li>number of L1 read misses, <em>excluding L1 read misses that hit in the stream buffers if L1 prefetch unit is enabled </em></li>
<li>number of L1 writes</li>
<li>number of L1 write misses, <em>excluding L1 write misses that hit in the stream buffers if L1 prefetch unit is enabled </em></li>
<li>L1 miss rate = MR<sub>L1</sub> = (L1 read misses + L1 write misses)/(L1 reads + L1 writes)</li>
<li>number of writebacks from L1 to next level</li>
<li>number of L1 prefetches (<em>prefetch requests from L1 to next level, if prefetch unit is enabled</em>)</li>
<li>number of L2 reads that did not originate from L1 prefetches (<em>should match b+d: L1 read misses + L1 write misses</em>)</li>
<li>number of L2 read misses that did not originate from L1 prefetches, <em>excluding such L2 read misses that hit in the stream buffers if L2 prefetch unit is enabled</em></li>
<li>number of L2 reads that originated from L1 prefetches (<em>should match g: L1 prefetches</em>)
<ul>
<li>SEE IMPORTANT NOTE BELOW.</li>
</ul>
</li>
<li>number of L2 read misses that originated from L1 prefetches, <em>excluding such L2 read misses that hit in the stream buffers if L2 prefetch unit is enabled </em>
<ul>
<li>SEE IMPORTANT NOTE BELOW.</li>
</ul>
</li>
<li>number of L2 writes (<em>should match f: number of writebacks from L1</em>)</li>
<li>number of L2 write misses, <em>excluding L2 write misses that hit in the stream buffers if L2 prefetch unit is enabled</em></li>
<li>L2 miss rate (<em>from standpoint of stalling the CPU</em>) = MR<sub>L2</sub> = (item i)/(item h)</li>
<li>number of writebacks from L2 to memory</li>
<li>number of L2 prefetches (<em>prefetch requests from L2 to next level, if prefetch unit is enabled</em>)</li>
<li>total memory traffic = number of blocks transferred to/from memory</li>
</ol>
(<em>with L2,</em> <em>should match i+k+m+o+p: </em>

<em>&nbsp;all L2 read misses + L2 write misses + writebacks from L2 + L2 prefetches</em>) (<em>without L2, should match b+d+f+g: </em>

<em>&nbsp;L1 read misses + L1 write misses + writebacks from L1 + L1 prefetches</em>)

&nbsp;

† For this project, as shown in Figure 5 for ECE 563 students, prefetching is only tested and explored in the last-level cache of the memory hierarchy. This means that measurements j and k, above, should always be 0 because the L1 will not issue prefetch requests to the L2. Nonetheless, a well-done implementation of a generic CACHE will distinguish incoming <em>demand read requests</em> from incoming <em>prefetch read requests</em>, even though in <em>this</em> project the distinction will not be exercised.

&nbsp;

<strong>Note for ECE 463 students: Just assume and print 0 for any prefetch-specific measurement. These are: g, j, k, p. </strong>

&nbsp;

<h2>8. Submit, Validate, and Self-Grade with Gradescope</h2>
Sample simulation outputs are provided on the Moodle site. These are called “validation runs”. <strong>Refer to the validation runs to see how to format the outputs of your simulator.</strong>

&nbsp;

<strong>You must submit, validate, and self-grade<a href="#_ftn2" name="_ftnref2"><sup>[2]</sup></a> your project using Gradescope.</strong> Here is how Gradescope (1) receives your project (zip file), (2) compiles your simulator (Makefile), and (3) runs and checks your simulator (arguments, print-to-console requirement, and “diff -iw”):

&nbsp;

<ol>
<li><strong>How Gradescope receives your project: zip file.</strong> While you are developing your simulator, you may continuously submit new zip files to Gradescope containing the latest version of your project. The latest submission is the one that is considered for your grade. Gradescope will accept a zip file consisting of three things: your source code, a Makefile to compile your source code, and your project report. In the early stages of your project, before creating the report, your zip file will have only source code and a Makefile. Once the report is completed, your zip file will contain everything.</li>
<li><u>Report (included in the zip file once available):</u> The report must be a PDF file named “report.pdf” located at the top level of the zip file, because that is what Gradescope looks for when checking completeness of the submission. The report must include the following: <em>See Section 9 and the report template in Moodle for the required contents of the report.</em>
<ul>
<li><u>Makefile:</u> The Makefile must be at the top level of the zip file, because Gradescope runs “make” with the expectation that the Makefile is at the top level.</li>
<li><u>Source code:</u> Whether your source code is at the top level of the zip file or in directories below the top level, your Makefile must be designed to compile your source code, accordingly.</li>
</ul>
</li>
</ol>
&nbsp;

<ol start="2">
<li><strong>How Gradescope compiles your simulator: Makefile.</strong> Along with your source code, you must provide a Makefile that automatically compiles the simulator. This Makefile must create a simulator named “sim”. An example Makefile is posted on the Moodle site, which you can copy and modify for your needs.</li>
</ol>
&nbsp;

<ol start="3">
<li><strong>How Gradescope runs and checks your simulator: arguments, print-to-console requirement, “diff -iw”, and timeout.</strong>
<ul>
<li>Your simulator executable (created by your Makefile) must be named “sim” and take command-line arguments in the manner specified in Section 6.2, because Gradescope assumes these things.</li>
<li>Your simulator must print outputs to the console (<em>e.</em>, to the screen), because Gradescope assumes this.</li>
<li>Your output must match the validation runs both <u>numerically</u> and in terms of <u>formatting</u>, because Gradescope runs “diff -iw” to compare your output with the correct output. The iw flags tell “diff” to treat upper-case and lower-case as equivalent and to ignore the amount of whitespace between words. Therefore, you do not need to worry about the</li>
</ul>
</li>
</ol>
&nbsp;

exact number of spaces or tabs as long as there is some whitespace where the validation runs have whitespace. Note, however, that extra or missing blank lines are NOT ok: “diff -iw” does not ignore extra or missing blank lines.

<ul>
<li>Gradescope’s autograder has a timeout for compiling the simulator and running all tests. The default timeout is 10 minutes. This is usually ample time for this course. If the autograder times out for your project (very inefficient simulator or a bug that causes deadlock), you will see a grade of zero for that submission. Please see Section 12.2 regarding optimizing run time. Also seek advice from the instructor and TAs, as needed.</li>
</ul>
&nbsp;

<h2>9. Experiments and Report</h2>
&nbsp;

See the <u>report template</u> in Moodle for experiments, graphs, and analysis.&nbsp; Use the report template as the basis for the report that you submit (insert graphs, fill in answers to questions, <em>etc</em>.).&nbsp; Below, you will find information about calculating AAT, area, and energy, for a given memory hierarchy configuration.

&nbsp;

<strong>Calculating AAT, Area, and Energy </strong>

&nbsp;

Table 1 gives names and descriptions of parameters and how to get these parameters.

&nbsp;

&nbsp;

<strong>Table 1. Parameters, descriptions, and how you obtain these parameters. </strong>

<table width="638">
<tbody>
<tr>
<td width="91"><em>Parameter </em></td>
<td width="264"><em>Description </em></td>
<td width="283"><em>How to get parameter </em></td>
</tr>
<tr>
<td width="91">MRL1</td>
<td width="264">L1 miss rate.</td>
<td rowspan="2" width="283">From your simulator. See Section 7.</td>
</tr>
<tr>
<td width="91">MRL2</td>
<td width="264">L2 miss rate (from standpoint of stalling the CPU).</td>
</tr>
<tr>
<td width="91">HTL1</td>
<td width="264">Hit time of L1.</td>
<td rowspan="2" width="283">Refer to the spreadsheet of CACTI results available on the Project-1 website: sheet “CACTI results”, column E “Access time (ns)”.</td>
</tr>
<tr>
<td width="91">HTL2</td>
<td width="264">Hit time of L2.</td>
</tr>
<tr>
<td width="91">Miss_Penalty</td>
<td width="264">Time to fetch one block from main memory.</td>
<td width="283">Refer to the spreadsheet of CACTI results available on the Project-1 website: sheet “Miss_Penalty”, cell B1.</td>
</tr>
<tr>
<td width="91">AL1</td>
<td width="264">Die area of L1.</td>
<td rowspan="2" width="283">Refer to the spreadsheet of CACTI results available on the Project-1 website: sheet “CACTI results”, column G “Area (mm*mm)”.</td>
</tr>
<tr>
<td width="91">AL2</td>
<td width="264">Die area of L2.</td>
</tr>
<tr>
<td width="91">EL1</td>
<td width="264">Dynamic energy per access of L1.</td>
<td rowspan="2" width="283">“Energy Per Access (nJ)” from CACTI tool. A spreadsheet of CACTI results is available on the Project-1 website.</td>
</tr>
<tr>
<td width="91">EL2</td>
<td width="264">Dynamic energy per access of L2.</td>
</tr>
<tr>
<td width="91">EMEM</td>
<td width="264">Dynamic energy per access of main memory.</td>
<td width="283">Refer to the spreadsheet of CACTI results available on the Project-1 website: sheet “E_MEM”.</td>
</tr>
</tbody>
</table>
* We will not be using energy in any of the experiments for this semester’s Project 1. Thus, they are grayed-out in Table 1.

&nbsp;

For memory hierarchy <em>without</em> L2 cache:

&nbsp;

Total access time <sub>=</sub> (L1 reads <sub>+</sub> L1 writes)<sub>⋅ </sub>HT<sub>L1 </sub>+ (L1 read misses <sub>+</sub> L1 write misses)<sub>⋅ </sub>Miss_Penalty

&nbsp;

<table width="215">
<tbody>
<tr>
<td rowspan="2" width="215">Average access time (AAT) = Total access time

(L1 reads <sub>+</sub> L1 writes)
</td>
<td width="0"></td>
</tr>
<tr>
<td width="0"></td>
</tr>
</tbody>
</table>
AAT <sub>= </sub>HTL1 <sub>+ </sub><sub> </sub><u>L1 read</u>L1<u> misses</u> reads <sub>+</sub>+<u> L1</u>L1<u> write</u> writes<u> misses</u><sub> ⋅ </sub>Miss_Penalty

<sub></sub>

= HT<sub>L1 </sub>+ MR<sub>L1 </sub>⋅ Miss_Penalty

&nbsp;

For memory hierarchy <em>with</em> L2 cache:

&nbsp;

Total access time <sub>=</sub> (L1 reads <sub>+</sub> L1 writes)<sub>⋅ </sub>HT<sub>L1 </sub>+ (L1 read misses <sub>+</sub> L1 write misses)<sub>⋅ </sub>HT<sub>L2 </sub>+ (L2 read misses not originating from L1 prefetches)<sub>⋅ </sub>Miss_Penalty

&nbsp;

<table width="215">
<tbody>
<tr>
<td rowspan="2" width="215">Average access time (AAT) = Total access time

(L1 reads <sub>+</sub> L1 writes)
</td>
<td width="0"></td>
</tr>
<tr>
<td width="0"></td>
</tr>
</tbody>
</table>
&nbsp;

AAT <sub>= </sub>HTL1 <sub>+</sub><sub> </sub><u>L1 read</u>L1<u> misses</u> reads <sub>+</sub>+ L1<u>L1</u> writes<u> write misses</u><sub>⋅</sub>HTL2 <sub>+</sub> <u>L2 read misses </u>L1<u>not </u>&nbsp;reads<u>originatin</u><sub>+ </sub>L1 writes<u>g from L1 prefetches</u><sub></sub><sub>⋅</sub>Miss_Penalty <sub></sub>

<sub>= </sub>HTL1 <sub>+ </sub>MRL1 <sub>⋅</sub>HTL2 <sub>+</sub><sub></sub> <u>L2 read misses </u>L1<u>not </u>&nbsp;reads<u>originatin</u><sub>+ </sub>L1 writes<u>g from L1 prefetches</u><sub></sub><sub>⋅</sub>Miss_Penalty

<sub>= </sub>HTL1 <sub>+ </sub>MRL1 <sub>⋅</sub><sub></sub>HTL2 <sub>+</sub><sub></sub> MR1 L1 <sub>⋅</sub><sub> </sub><u>L2 read misses </u>L1<u>not </u>&nbsp;reads<u>originatin</u><sub>+ </sub>L1 writes<u>g from L1 prefetches</u><sub>⋅</sub>Miss_Penalty<sub></sub>

= HTL1 + MRL1 ⋅<sub></sub>HTL2 +<sub></sub> L1 readL1 misses reads +<sub>+</sub> L1L1 writes write misses<sub></sub><sub></sub>⋅<sub></sub><sub> </sub><u>L2 read misses </u>L1<u>not </u>&nbsp;reads<u>originatin</u><sub>+ </sub>L1 writes<u>g from L1 prefetches</u><sub></sub><sub></sub>⋅Miss_Penalty<sub></sub>

<sub>= </sub>HTL1 <sub>+ </sub>MRL1 <sub>⋅</sub><sub></sub>HTL2 <sub>+</sub><sub></sub> <u>L2 read misses</u>L1 read<u> not </u>&nbsp;misses<u>originatin</u> <sub>+</sub> L1 write<u>g from</u> misses<u> L1 prefetches</u><sub>⋅</sub>Miss_Penalty<sub></sub>

= HTL1 + MRL1 ⋅<sub></sub>HTL2 +<sub></sub> <u>L2 </u>L2<u>read</u> reads<u> misses</u> not <u>&nbsp;not </u>originatin<u>originatin</u>g from<u>g from</u> L1 <u>&nbsp;</u>prefetches<u>L1 prefetches</u><sub></sub>⋅Miss_Penalty<sub></sub>

= HT<sub>L1 </sub>+ MR<sub>L1 </sub>⋅(HT<sub>L2 </sub>+ MR<sub>L2 </sub>⋅Miss_Penalty)

&nbsp;

&nbsp;

The total area of the caches:

Area = A<sub>L1 </sub>+ A<sub>L2</sub>

If a particular cache does not exist in the memory hierarchy configuration, then its area is 0. Note that it is difficult to estimate the area of the prefetch unit using CACTI due to the specialized structure of the Stream Buffers.

&nbsp;

&nbsp;

Dynamic energy estimates:

Each read or write request to a cache consumes that cache’s access energy. Each read or write request that misses in the cache causes a “line fill” (allocation) into the cache, which also consumes that cache’s access energy.<a href="#_ftn3" name="_ftnref3"><sup>[3]</sup></a> Each writeback of an evicted dirty block involves reading that block from the cache, which also consumes that cache’s access energy.

&nbsp;

For memory hierarchy <em>without</em> L2 cache:

&nbsp;

Total dynamic energy =

(L1 reads + L1 writes + L1 read misses + L1 write misses + L1 writebacks) * E<sub>L1</sub> + (L1 read misses + L1 write misses + L1 writebacks + L1 prefetches) * E<sub>MEM</sub>

&nbsp;

For memory hierarchy <em>with</em> L2 cache:

&nbsp;

Total dynamic energy =

(L1 reads + L1 writes + L1 read misses + L1 write misses + L1 writebacks) * E<sub>L1</sub> +

(<u>all</u> L2 reads + L2 writes + <u>all</u> L2 read misses + L2 write misses + L2 writebacks) * E<sub>L2</sub> + (<u>all</u> L2 read misses + L2 write misses + L2 writebacks + L2 prefetches) * E<sub>MEM</sub>

&nbsp;

&nbsp;

average dynamic energy per access = (total dynamic energy)/(L1 reads + L1 writes)

&nbsp;

&nbsp;

<h2>10. Grading</h2>
Table 2 shows the breakdown of points for the project:

<strong>[30 points]</strong> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp; <strong>Substantial programming effort.</strong>

<strong>[50 points]</strong> &nbsp;&nbsp;&nbsp;&nbsp; <strong>A working simulator</strong>, as determined by matching validation runs.

<strong>[20 points]</strong> <strong>Experiments and report.</strong> You can only get credit for experiments with L1 if your simulator passes BOTH validation runs #1 and #2. You can only get credit for L1+L2 experiments if your simulator passes BOTH validation runs #3 and #4. You can only get credit for L1+pref experiments if your simulator passes BOTH validation runs #5 and #6.

&nbsp;

<strong>Table 2.&nbsp; Breakdown of points. </strong>

<strong>[30 points]&nbsp; Substantial programming effort. </strong>

<table width="638">
<tbody>
<tr>
<td width="319"><strong>Item </strong></td>
<td width="160"><strong>Points (ECE 463) </strong></td>
<td width="160"><strong>Points (ECE 563) </strong></td>
</tr>
<tr>
<td width="319">Cache class code: see next page for partial credit rubric.</td>
<td width="160">0 – 30 points</td>
<td width="160">0 – 30 points</td>
</tr>
</tbody>
</table>
&nbsp;

<strong>[50 points]&nbsp; A working simulator: match validation runs. </strong>

<table width="638">
<tbody>
<tr>
<td colspan="2" width="319"><strong>Item </strong></td>
<td width="160"><strong>Points (ECE 463) </strong></td>
<td width="160"><strong>Points (ECE 563) </strong></td>
</tr>
<tr>
<td rowspan="3" width="160">L1 works</td>
<td width="160">validation run #1</td>
<td width="160">9 points</td>
<td width="160">6 points</td>
</tr>
<tr>
<td width="160">validation run #2</td>
<td width="160">9 points</td>
<td width="160">7 points</td>
</tr>
<tr>
<td width="160">mystery run A</td>
<td width="160">8 points</td>
<td width="160">7 points</td>
</tr>
<tr>
<td rowspan="3" width="160">L1, L2 works</td>
<td width="160">validation run #3</td>
<td width="160">8 points</td>
<td width="160">6 points</td>
</tr>
<tr>
<td width="160">validation run #4</td>
<td width="160">8 points</td>
<td width="160">7 points</td>
</tr>
<tr>
<td width="160">mystery run B</td>
<td width="160">8 points</td>
<td width="160">7 points</td>
</tr>
<tr>
<td rowspan="3" width="160">L1+pref. works</td>
<td width="160">validation run #5</td>
<td rowspan="6" width="160"><em>not applicable</em></td>
<td width="160">2 points</td>
</tr>
<tr>
<td width="160">validation run #6</td>
<td width="160">2 points</td>
</tr>
<tr>
<td width="160">mystery run C</td>
<td width="160">2 points</td>
</tr>
<tr>
<td rowspan="3" width="160">L1, L2+pref. works</td>
<td width="160">validation run #7</td>
<td width="160">2 points</td>
</tr>
<tr>
<td width="160">validation run #8</td>
<td width="160">1 points</td>
</tr>
<tr>
<td width="160">mystery run D</td>
<td width="160">1 points</td>
</tr>
</tbody>
</table>
&nbsp;

<strong>[20 points]&nbsp; Experiments and report. </strong>

<table width="638">
<tbody>
<tr>
<td width="151">&nbsp;</td>
<td width="168"><strong>Item </strong></td>
<td width="160"><strong>Points (ECE 463) </strong></td>
<td width="160"><strong>Points (ECE 563) </strong></td>
</tr>
<tr>
<td rowspan="6" width="151">Experiments and Report</td>
<td width="168">GRAPH #1 + disc.</td>
<td width="160">5 points</td>
<td width="160">4 points</td>
</tr>
<tr>
<td width="168">GRAPH #2 + disc.</td>
<td width="160">3 points</td>
<td width="160">3 points</td>
</tr>
<tr>
<td width="168">GRAPH #3 + disc.</td>
<td width="160">4 points</td>
<td width="160">4 points</td>
</tr>
<tr>
<td width="168">GRAPH #4 + disc.</td>
<td width="160">4 points</td>
<td width="160">3 points</td>
</tr>
<tr>
<td width="168">GRAPH #5 + disc.</td>
<td width="160">4 points</td>
<td width="160">3 points</td>
</tr>
<tr>
<td width="168">TABLE #1 + disc.</td>
<td width="160"><em>not applicable</em></td>
<td width="160">3 points</td>
</tr>
</tbody>
</table>
&nbsp;

Analysis:

463 max points with just L1 working and corresponding graphs+discussion (#1,2,4): 56 (sim.) + 12 (exp.) = 68

563 max points with just L1 working and corresponding graphs+discussion (#1,2,4): 50 (sim.) + 10 (exp.) = 60

563 max points with everything but pref. working, and corr. graphs+discussion (#1-5): 70 (sim.) + 17 (exp.) = 87

563 max points with everything but L2 working, and corr. graphs+discussion (#1,2,4,T1): 56 (sim.) + 13 (exp.) = 69

<strong>Grading of “Substantial programming effort”: </strong>

&nbsp;

If your simulator passes at least one validation run, the TAs will automatically credit 30 points for “Substantial programming effort”.

&nbsp;

If your simulator does not match any validation runs, you can receive between 0 and 30 points for “Substantial programming effort” depending on how many implementation aspects are covered.&nbsp; The TAs will use the rubric below for assessing partial credit for implementation effort of a basic cache class.&nbsp; To get credit for a given rubric item, the code attempt must be valid and substantial.

&nbsp;

Note that the 0 – 30 points for implementation effort covers only a basic cache class.&nbsp; On the positive side, this incentivizes students to at least attempt to get an L1 cache fully working and get credit for experiments with L1 only.&nbsp; On the other hand, as a counterexample, suppose a 563 student strives to get their prefetcher working but fails to match any validation runs with prefetchers; there is no partial credit for implementation effort of the prefetcher itself; the incentive for the student to code the prefetcher and get it working, is the additional point value of passing the prefetcher validation runs and the point value of the associated experiments.

<strong>Other notes about grading: </strong>

&nbsp;

<ul>
<li>You can only get credit for a given experiment/graph/analysis, if you pass ALL validation runs corresponding with that experiment/graph/analysis. For example, if a given experiment/graph/analysis requires simulations with L1+L2, you can only get credit for this experiment/graph/analysis if you pass <u>both</u> validation runs #3 and #4.</li>
<li>If your simulator doesn’t match a given validation run, it doesn’t matter how many measurements differ, which measurements differ, and the amount by which the measurements differ. It doesn’t matter if it’s just a formatting issue, either.&nbsp; It doesn’t matter if the bug is just one line of code, one tiny thing, <em>etc</em>.&nbsp; As an extreme example, suppose you are off by just one L1 writeback in both validation run #1 and validation run #2, which test L1 cache only.&nbsp; You will not get any points for these validation runs (you are self-grading via Gradescope).&nbsp; Moreover, you cannot receive any credit for experiments/graphs/analysis that require simulations with L1 cache only, even though L1 writebacks to main memory have no bearing on L1 miss rate, AAT, <em>etc</em>.&nbsp; This may seem harsh but it is fair for all students.&nbsp; It is the only sure, fair, and practical way to grade projects.&nbsp; Also, being exacting will benefit you and future employers in the long run.</li>
<li>Students may observe that their measurements are off and yet their final cache and prefetcher contents match exactly. This is not contradictory and quite possible, because the final cache/prefetcher contents only reflect the most recent references in the trace. The measurement errors could be due to incorrect intermediate cache/prefetcher contents in the distant past (or measurement counting bugs).</li>
</ul>
&nbsp;

<h2>11. Penalties</h2>
&nbsp;

Various deductions (out of 100 points):

&nbsp;

<strong>-1 point</strong> for each day (24-hour period) late, according to the Gradescope timestamp. The late penalty is pro-rated on an hourly basis: -1/24 point for each hour late. We will use the “ceiling” function of the lateness time to get to the next higher hour, <em>e.g.</em>, ceiling(10 min. late) = 1 hour late, ceiling(1 hr, 10 min. late) = 2 hours late, and so forth. <strong>For this first project, Gradescope will accept late submissions no more than two weeks after the deadline. The goal of this policy is to encourage forward progress for other work in the class.</strong>

&nbsp;

<strong>See Section 1.1 for penalties and sanctions for academic integrity violations</strong>.

&nbsp;

<h2>12. Advice on backups and run time</h2>
<h3>12.1. Keeping backups</h3>
It is good practice to frequently make backups of all your project files, including source code, your report, <em>etc</em>.&nbsp; You can backup files to another hard drive (your NFS B: drive in your NCSU account, home PC, laptop … keep consistent copies in multiple places) or removable media

(flash drive, <em>etc</em>.).

<h3>12.2. Run time of simulator</h3>
<em>Correctness</em> of your simulator is of paramount importance. That said, making your simulator <em>efficient</em> is also important because you will be running many experiments: many memory hierarchy configurations and multiple traces. Therefore, you will benefit from implementing a simulator that is reasonably fast.

&nbsp;

One simple thing you can do to make your simulator run faster is to compile it with a high optimization level. The example Makefile posted on the Moodle site includes the –O3 optimization flag.

&nbsp;

Note that, when you are debugging your simulator in a debugger (such as gdb), it is recommended that you compile without –O3 and with –g. Optimization includes register allocation. Often, register-allocated variables are not displayed properly in debuggers, which is why you want to disable optimization when using a debugger. The –g flag tells the compiler to include symbols (variable names, <em>etc</em>.) in the compiled binary. The debugger needs this information to recognize variable names, function names, line numbers in the source code, <em>etc</em>. When you are done debugging, recompile with –O3 and without –g, to get the most efficient simulator again.

&nbsp;

As mentioned in Section 8, another reason for being wary of excessive run times is Gradescope’s autograder timeout.

<a href="#_ftnref1" name="_ftn1">[1]</a> For accurate performance accounting using the Average Access Time (AAT) expression, you will need to convey to the next level in the memory hierarchy that these read requests are prefetches. This will enable the next level in the memory hierarchy to distinguish between 1) its read misses that originated from normal read requests versus 2) its read misses that originated from prefetch read requests. Note that this is only needed for accurate performance accounting.

<a href="#_ftnref2" name="_ftn2">[2]</a> The mystery runs component of your grade will not be published until we release it.&nbsp; The report will be manually graded by the TAs.

<a href="#_ftnref3" name="_ftn3">[3]</a> Note: There is a noticeable underestimate of energy when a request misses in the cache but hits in its stream buffer. We don’t count this as a miss (it doesn’t get counted as an L1 read miss or L1 write miss) and we don’t explicitly count this scenario. Yet, this scenario also involves a “line fill” (allocation) into the cache (transfer block from stream buffer to cache). This can be fixed by explicitly counting this scenario but we shall ignore it in this project.
