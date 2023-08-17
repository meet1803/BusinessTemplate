<script>
  import img1 from "../images/img1.jpg";
  import img2 from "../images/img2.jpg";
  import img3 from "../images/img3.jpg";
  import img4 from "../images/img4.jpg";
  import logo from "../images/logo-main.png";
  import NavBar from "./NavBar.svelte";
  import Icon from "@iconify/svelte";

  const ImageList = [
    { link: img1 },
    { link: img2 },
    { link: img3 },
    { link: img4 },
  ];

  const NavItemList = [
    { name: "Page", link: "/Page" },
    { name: "Portfolio", link: "/Portfolio" },
    { name: "Blog", link: "/Blog" },
    { name: "Shop", link: "/Shop" },
  ];

  let currentImageIndex = 0;
  let delay = 2000;

  function nextImage() {
    currentImageIndex = (currentImageIndex + 1) % ImageList.length;
  }

  function startSlideshow() {
    setInterval(nextImage, delay);
  }

  startSlideshow();

</script>

<header class="mx-auto items-center justify-between">
  <nav class="mx-auto items-center justify-between ">
    <div class="mr-4">
      {#each ImageList as item, i}
        {#if i === currentImageIndex}
          <img
            src={item.link}
            class=" absolute mix-blend-overlay"
            alt="images"
          />

          <div class="h-10 backdrop-blur-lg flex gap-5 justify-start mr-6">
            <div class=" pt-2 flex gap-2 ">
              <span class="lg:ml-11 mt-1">
                <svg
                  xmlns="http://www.w3.org/2000/svg"
                  width="13"
                  height="13"
                  viewBox="0 0 15 15"
                  ><path
                    fill="white"
                    d="M7.303.04a.5.5 0 0 1 .394 0L14.5 2.956l-7 3l-7-3L7.303.04ZM0 3.83v7.67c0 .2.12.38.303.46L7 14.83v-8l-7-3Zm8 3l7-3v7.67a.5.5 0 0 1-.303.46L8 14.83v-8Z"
                  /></svg
                >
              </span>

              <p class="text-[13px] font-normal" style="color: #ffffffb3;">
                Leroux - For all
                <a
                  href="https://leroux.qodeinteractive.com/our-services/"
                  class="underline underline-offset-4">your business</a
                >
                endeavors
              </p>
            </div>

            <div class="flex gap-5 ml-96 pl-8">
              <div class="flex pt-2 gap-2">
                <span class="lg:mt-1">
                <svg
                  xmlns="http://www.w3.org/2000/svg"
                  width="13"
                  height="13"
                  viewBox="0 0 24 24"
                  font-weight="bold"
                  ><path
                    fill="white"
                    d="M24 12v-.006c0-3.551-1.546-6.74-4.001-8.933l-.012-.01a.596.596 0 0 0-.101-.087l-.002-.001A11.917 11.917 0 0 0 11.998.001c-3.032 0-5.8 1.126-7.91 2.984l.013-.011a.481.481 0 0 0-.07.065v.001A11.959 11.959 0 0 0 0 12.003c0 3.55 1.544 6.739 3.997 8.933l.012.01a.672.672 0 0 0 .106.097l.002.001a11.92 11.92 0 0 0 7.881 2.958a11.93 11.93 0 0 0 7.911-2.984l-.013.011a11.94 11.94 0 0 0 4.106-9.021v-.007zm-4.462 7.805a11.935 11.935 0 0 0-1.909-1.262l-.065-.032c.613-1.767.982-3.804 1.017-5.923v-.016h4.261a10.824 10.824 0 0 1-3.301 7.23zM12.572 18.3c1.283.069 2.482.351 3.588.81l-.072-.026c-.886 2.02-2.133 3.408-3.516 3.713zm0-1.144v-4.584h4.868a18.593 18.593 0 0 1-.976 5.578l.039-.131a11.637 11.637 0 0 0-3.903-.862l-.027-.001zm0-5.728V6.844a11.91 11.91 0 0 0 4.007-.891l-.079.029c.555 1.619.896 3.485.94 5.425v.021zm0-5.728V1.205c1.383.305 2.63 1.687 3.516 3.713c-1.034.43-2.233.711-3.487.781zm2.854-4a10.841 10.841 0 0 1 3.258 1.752l-.023-.018c-.443.348-.94.676-1.464.961l-.056.028a10.07 10.07 0 0 0-1.724-2.737l.009.011zm-4-.492V5.7a10.804 10.804 0 0 1-3.588-.81l.072.026c.89-2.02 2.135-3.407 3.518-3.712zM6.858 4.42a10.943 10.943 0 0 1-1.544-1.007l.024.018a10.744 10.744 0 0 1 3.158-1.712l.076-.023a10.02 10.02 0 0 0-1.689 2.658l-.025.065zm4.57 2.423v4.584H6.56c.044-1.961.385-3.827.979-5.577l-.039.131a11.65 11.65 0 0 0 3.901.861zm0 5.728v4.584a11.91 11.91 0 0 0-4.007.891l.079-.029c-.555-1.618-.896-3.485-.94-5.425v-.021zm0 5.728v4.495c-1.383-.305-2.63-1.687-3.516-3.713c1.034-.43 2.233-.71 3.487-.78l.029-.001zm-2.85 4a10.845 10.845 0 0 1-3.258-1.748l.024.018c.443-.348.94-.676 1.464-.961l.056-.028a9.843 9.843 0 0 0 1.723 2.733l-.009-.01zm8.564-2.72c.58.315 1.077.642 1.544 1.007l-.024-.018a10.744 10.744 0 0 1-3.158 1.712l-.076.023a10.014 10.014 0 0 0 1.689-2.657l.025-.065zm5.7-8.151h-4.261a19.663 19.663 0 0 0-1.058-6.078l.041.138a12.383 12.383 0 0 0 1.997-1.312l-.024.018a10.813 10.813 0 0 1 3.303 7.205l.001.028zM4.462 4.195c.576.468 1.223.897 1.909 1.262l.065.032c-.613 1.767-.982 3.804-1.017 5.923v.016H1.157a10.824 10.824 0 0 1 3.301-7.23l.003-.003zm-3.304 8.377h4.261a19.663 19.663 0 0 0 1.058 6.078l-.041-.138c-.751.399-1.397.828-1.997 1.312l.024-.018a10.813 10.813 0 0 1-3.303-7.205l-.001-.028z"
                  /></svg
                >
                </span>

                <p class="text-[13px] font-normal" style="color: #ffffffb3;">
                  Mon - Frd : 8:00-16:00
                </p>
              </div>

              <div class="flex pt-2 gap-2">
                <span class="lg:mt-1">
                  <svg
                    xmlns="http://www.w3.org/2000/svg"
                    width="13"
                    height="13"
                    viewBox="0 0 20 20"
                    font-weight="bold"
                    ><path
                      fill="white"
                      fill-rule="evenodd"
                      d="M18.333 2.5c.92 0 1.667.746 1.667 1.667v11.666c0 .92-.746 1.667-1.667 1.667H1.667C.747 17.5 0 16.754 0 15.833V4.167C0 3.247.746 2.5 1.667 2.5h16.666ZM7.168 11.328l-4.91 4.852h15.325l-4.857-4.802L10 13.265l-2.832-1.937ZM18.64 7.292l-4.796 3.316l4.796 4.736V7.292Zm-17.279.061v7.836l4.686-4.631l-4.686-3.205Zm16.956-3.532H1.698a.358.358 0 0 0-.25.086a.26.26 0 0 0-.085.222v1.62L10 11.656l8.644-5.965V4.199c.001-.134-.03-.231-.092-.292a.306.306 0 0 0-.234-.086Z"
                    /></svg
                  >
                </span>

                <p class="text-[13px] font-normal" style="color: #ffffffb3;">
                  <a href="/">leroux@example.com</a>
                </p>
              </div>
            </div>
          </div>

          <div class="mx-auto flex items-center">
            <div class="justify-start basis-1/2 ml-11 lg:mt-8">
              <a href="/">
                <img src={logo} class="h-6" alt="leroux" />
              </a>
            </div>

            <div
              class="flex items-center justify-center lg:mt-8 gap-1 text-white"
            >
              <NavBar name="Home" link="/" />
              {#each NavItemList as item}
                <NavBar name={item.name} link={item.link} />
              {/each}

              <div class="lg:flex gap-5">
                <button
                  class="rounded-full w-44 h-11 lg:ml-3 backdrop-blur-3xl"
                >
                  <a
                    href="https://leroux.qodeinteractive.com/get-in-touch/"
                    class="lg:text-base font-semibold"
                  >
                    <span class=" font-normal"> Get In Touch </span>
                  </a>
                </button>

                <button class="cursor-pointer">
                  <a href="/">
                    <div class="lg:mt-1">
                      <Icon class="w-6 h-6" icon="ant-design:search-outline" />
                    </div>
                  </a>
                </button>

                <button class="cursor-pointer">
                  <div class="border-b-[1px] w-11" />
                  <div class="border-b-[1px] w-11 mt-2" />
                </button>
              </div>
            </div>
          </div>
          <div class="border-b-[1px] border-b-zinc-400 lg:ml-11 lg:mt-5 lg:mr-6" />
        {/if}
      {/each}
    </div>
  </nav>
</header>
