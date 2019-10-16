---
title: Azure hitelesítő adatok megőrzése a PowerShell-munkamenetek között
description: A cikkből megismerheti, hogyan használhatók fel újra az Azure-beli hitelesítő és egyéb adatok több PowerShell-munkamenet során.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 12/13/2018
ms.openlocfilehash: 02b8090aa1868f24445ddff3a95c0d0c376e2cb8
ms.sourcegitcommit: 0b94b9566124331d0b15eb7f5a811305c254172e
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/15/2019
ms.locfileid: "72370410"
---
# <a name="persist-azure-user-credentials-across-powershell-sessions"></a><span data-ttu-id="6bf8c-103">Azure-felhasználói hitelesítő adatok megőrzése a PowerShell-munkamenetek között</span><span class="sxs-lookup"><span data-stu-id="6bf8c-103">Persist Azure user credentials across PowerShell sessions</span></span>

<span data-ttu-id="6bf8c-104">Az Azure PowerShell új, **Azure-környezet automatikus mentése** nevű funkciója a következő szolgáltatásokat nyújtja:</span><span class="sxs-lookup"><span data-stu-id="6bf8c-104">Azure PowerShell offers a feature called **Azure Context Autosave**, which gives the following features:</span></span>

- <span data-ttu-id="6bf8c-105">A bejelentkezési adatok megőrzése és ismételt használata az új PowerShell-munkamenetekben.</span><span class="sxs-lookup"><span data-stu-id="6bf8c-105">Retention of sign-in information for reuse in new PowerShell sessions.</span></span>
- <span data-ttu-id="6bf8c-106">A háttérfeladatok egyszerűbb használata a hosszú ideig futó parancsmagok végrehajtásához.</span><span class="sxs-lookup"><span data-stu-id="6bf8c-106">Easier use of background tasks for executing long-running cmdlets.</span></span>
- <span data-ttu-id="6bf8c-107">Váltás a fiókok, előfizetések és környezet között külön bejelentkezés nélkül.</span><span class="sxs-lookup"><span data-stu-id="6bf8c-107">Switch between accounts, subscriptions, and environments without a separate sign-in.</span></span>
- <span data-ttu-id="6bf8c-108">Feladatok egyidejű végrehajtása több bejelentkezés és előfizetés használatával ugyanabból a PowerShell-munkamenetből.</span><span class="sxs-lookup"><span data-stu-id="6bf8c-108">Execution of tasks using different credentials and subscriptions, simultaneously, from the same PowerShell session.</span></span>

## <a name="azure-contexts-defined"></a><span data-ttu-id="6bf8c-109">Az Azure-környezetek</span><span class="sxs-lookup"><span data-stu-id="6bf8c-109">Azure contexts defined</span></span>

<span data-ttu-id="6bf8c-110">Az *Azure-környezet* az Azure PowerShell-parancsmagok célját meghatározó adatok halmaza.</span><span class="sxs-lookup"><span data-stu-id="6bf8c-110">An *Azure context* is a set of information that defines the target of Azure PowerShell cmdlets.</span></span> <span data-ttu-id="6bf8c-111">A környezet öt részből áll:</span><span class="sxs-lookup"><span data-stu-id="6bf8c-111">The context consists of five parts:</span></span>

- <span data-ttu-id="6bf8c-112">A *Fiók* – Az Azure-beli kommunikáció hitelesítéséhez használt felhasználónév vagy szolgáltatásnév</span><span class="sxs-lookup"><span data-stu-id="6bf8c-112">An *Account* - the UserName or Service Principal used to authenticate communications with Azure</span></span>
- <span data-ttu-id="6bf8c-113">Az *előfizetés* – Az adott erőforrásokat tartalmazó Azure-előfizetés, amelyre a műveletek irányulnak.</span><span class="sxs-lookup"><span data-stu-id="6bf8c-113">A *Subscription* - The Azure Subscription with the Resources being acted upon.</span></span>
- <span data-ttu-id="6bf8c-114">A *bérlő* – Az előfizetést tartalmazó Azure Active Directory-bérlő.</span><span class="sxs-lookup"><span data-stu-id="6bf8c-114">A *Tenant* - The Azure Active Directory tenant that contains your subscription.</span></span> <span data-ttu-id="6bf8c-115">A bérlők a szolgáltatásnévvel való hitelesítés során fontosabbak.</span><span class="sxs-lookup"><span data-stu-id="6bf8c-115">Tenants are more important to ServicePrincipal authentication.</span></span>
- <span data-ttu-id="6bf8c-116">A *környezet* – A célzott Azure-felhő, általában az Azure globális felhője.</span><span class="sxs-lookup"><span data-stu-id="6bf8c-116">An *Environment* - The particular Azure Cloud being targeted, usually the Azure global Cloud.</span></span>
  <span data-ttu-id="6bf8c-117">A környezetbeállításban azonban megadhat országos, kormányzati és helyszíni (Azure Stack) felhőket is.</span><span class="sxs-lookup"><span data-stu-id="6bf8c-117">However, the environment setting allows you to target National, Government, and on-premises (Azure Stack) clouds as well.</span></span>
- <span data-ttu-id="6bf8c-118">A *hitelesítő adatok* – Az Azure által az identitás és az Azure-erőforrások hozzáférési jogosultságának ellenőrzéséhez használt adatok.</span><span class="sxs-lookup"><span data-stu-id="6bf8c-118">*Credentials* - The information used by Azure to verify your identity and confirm your authorization to access resources in Azure</span></span>

<span data-ttu-id="6bf8c-119">Az Azure PowerShell legújabb verziójában új PowerShell-munkamenet megnyitásakor beállítható az Azure-környezetek automatikus mentése.</span><span class="sxs-lookup"><span data-stu-id="6bf8c-119">With the latest version of Azure PowerShell, Azure Contexts can automatically be saved whenever opening a new PowerShell session.</span></span>

## <a name="automatically-save-the-context-for-the-next-sign-in"></a><span data-ttu-id="6bf8c-120">A környezet automatikus mentése a következő bejelentkezéshez</span><span class="sxs-lookup"><span data-stu-id="6bf8c-120">Automatically save the context for the next sign-in</span></span>

<span data-ttu-id="6bf8c-121">Az Azure PowerShell automatikusan megőrzi a környezet adatait a munkamenetek között.</span><span class="sxs-lookup"><span data-stu-id="6bf8c-121">Azure PowerShell retains your context information automatically between sessions.</span></span> <span data-ttu-id="6bf8c-122">Ha szeretné beállítani, hogy a PowerShell elfelejtse a környezetet és a hitelesítő adatokat, használja a `Disable-AzContextAutoSave` parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="6bf8c-122">To set PowerShell to forget your context and credentials, use `Disable-AzContextAutoSave`.</span></span> <span data-ttu-id="6bf8c-123">Ha le van tiltva a környezet mentése, minden alkalommal be kell jelentkeznie az Azure-ba, amikor megnyit egy PowerShell-munkamenetet.</span><span class="sxs-lookup"><span data-stu-id="6bf8c-123">With context saving disabled, you'll need to sign in to Azure every time you open a PowerShell session.</span></span>

<span data-ttu-id="6bf8c-124">Ha szeretné engedélyezni, hogy az Azure PowerShell megjegyezze a környezet adatait a PowerShell-munkamenetek bezárásakor, használja az `Enable-AzContextAutosave` parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="6bf8c-124">To allow Azure PowerShell to remember your context after the PowerShell session is closed, use `Enable-AzContextAutosave`.</span></span> <span data-ttu-id="6bf8c-125">A rendszer automatikusan menti a környezet adatait és a hitelesítő adatokat egy speciális rejtett mappába a felhasználó könyvtárában (`$env:USERPROFILE\.Azure` Windows rendszeren és `$HOME/.Azure` más platformokon).</span><span class="sxs-lookup"><span data-stu-id="6bf8c-125">Context and credential information are automatically saved in a special hidden folder in your user directory (`$env:USERPROFILE\.Azure` on Windows, and `$HOME/.Azure` on other platforms).</span></span> <span data-ttu-id="6bf8c-126">Minden egyes új PowerShell-munkamenet az utolsó munkamenet során használt környezetre irányul.</span><span class="sxs-lookup"><span data-stu-id="6bf8c-126">Each new PowerShell session targets the context used in your last session.</span></span>

<span data-ttu-id="6bf8c-127">Az Azure-környezetek kezeléséhez használt parancsmagokkal pontosan szabályozható a működés.</span><span class="sxs-lookup"><span data-stu-id="6bf8c-127">The cmdlets that allow you to manage Azure contexts also allow you fine grained control.</span></span> <span data-ttu-id="6bf8c-128">Például megadhatja, hogy a módosítások csak az aktuális PowerShell-munkamenetre (`Process` hatókör) vagy minden PowerShell-munkamenetre (`CurrentUser` hatókör) érvényesek legyenek.</span><span class="sxs-lookup"><span data-stu-id="6bf8c-128">If you want changes to apply only to the current PowerShell session (`Process` scope) or every PowerShell session (`CurrentUser` scope).</span></span> <span data-ttu-id="6bf8c-129">Ezeket a beállításokat részletesebben a [Környezeti hatókörök használata](#using-context-scopes) című szakasz tárgyalja.</span><span class="sxs-lookup"><span data-stu-id="6bf8c-129">These options are discussed in more detail in [Using Context Scopes](#using-context-scopes).</span></span>

## <a name="running-azure-powershell-cmdlets-as-background-jobs"></a><span data-ttu-id="6bf8c-130">Azure PowerShell-parancsmagok futtatása háttérfeladatként</span><span class="sxs-lookup"><span data-stu-id="6bf8c-130">Running Azure PowerShell cmdlets as background jobs</span></span>

<span data-ttu-id="6bf8c-131">Az **Azure-környezet automatikus mentése** funkcióval megoszthatja a környezetet a PowerShell-háttérfeladatokkal.</span><span class="sxs-lookup"><span data-stu-id="6bf8c-131">The **Azure Context Autosave** feature also allows you to share you context with PowerShell background jobs.</span></span> <span data-ttu-id="6bf8c-132">A PowerShell segítségével a hosszú lefutású feladatokat indíthatja és monitorozhatja háttérfeladatokként is, így nem kell megvárnia, amíg ezek befejeződnek.</span><span class="sxs-lookup"><span data-stu-id="6bf8c-132">PowerShell allows you to start and monitor long-executing tasks as background jobs without having to wait for the tasks to complete.</span></span> <span data-ttu-id="6bf8c-133">A hitelesítő adatokat kétféleképpen oszthatja meg a háttérfeladatokkal:</span><span class="sxs-lookup"><span data-stu-id="6bf8c-133">You can share credentials with background jobs in two different ways:</span></span>

- <span data-ttu-id="6bf8c-134">A környezet átadása argumentumként</span><span class="sxs-lookup"><span data-stu-id="6bf8c-134">Passing the context as an argument</span></span>

  <span data-ttu-id="6bf8c-135">A legtöbb AzureRM-parancsmagba a környezet átadható a parancsmag paramétereként.</span><span class="sxs-lookup"><span data-stu-id="6bf8c-135">Most AzureRM cmdlets allow you to pass the context as a parameter to the cmdlet.</span></span> <span data-ttu-id="6bf8c-136">A környezet a háttérfeladat számára az alábbi példában látható módon adható át:</span><span class="sxs-lookup"><span data-stu-id="6bf8c-136">You can pass a context to a background job as shown in the following example:</span></span>

  ```powershell-interactive
  PS C:\> $job = Start-Job { param ($ctx) New-AzVm -AzureRmContext $ctx [... Additional parameters ...]} -ArgumentList (Get-AzContext)
  ```

- <span data-ttu-id="6bf8c-137">Az alapértelmezett környezet használata működő automatikus mentés mellett</span><span class="sxs-lookup"><span data-stu-id="6bf8c-137">Using the default context with Autosave enabled</span></span>

  <span data-ttu-id="6bf8c-138">Ha engedélyezte a **Környezet automatikus mentése** funkciót, a háttérfeladatok automatikusan az alapértelmezett mentett környezetet használják.</span><span class="sxs-lookup"><span data-stu-id="6bf8c-138">If you have enabled **Context Autosave**, background jobs automatically use the default saved context.</span></span>

  ```powershell-interactive
  PS C:\> $job = Start-Job { New-AzVm [... Additional parameters ...]}
  ```

<span data-ttu-id="6bf8c-139">Ha tájékozódni szeretne egy háttérfeladat kimeneteléről, a `Get-Job` parancsmaggal ellenőrizheti le a feladat állapotát, és a `Wait-Job` parancsmaggal várhatja meg a feladat befejezését.</span><span class="sxs-lookup"><span data-stu-id="6bf8c-139">When you need to know the outcome of the background task, use `Get-Job` to check the job status and `Wait-Job` to wait for the Job to complete.</span></span> <span data-ttu-id="6bf8c-140">A `Receive-Job` parancsmaggal rögzítheti és jelenítheti meg a háttérfeladat kimenetét.</span><span class="sxs-lookup"><span data-stu-id="6bf8c-140">Use `Receive-Job` to capture or display the output of the background job.</span></span> <span data-ttu-id="6bf8c-141">További információkért lásd a [feladatokat ismertető szakaszt](/powershell/module/microsoft.powershell.core/about/about_jobs).</span><span class="sxs-lookup"><span data-stu-id="6bf8c-141">For more information, see [about_Jobs](/powershell/module/microsoft.powershell.core/about/about_jobs).</span></span>

## <a name="creating-selecting-renaming-and-removing-contexts"></a><span data-ttu-id="6bf8c-142">Környezetek létrehozása, kiválasztása, átnevezése és eltávolítása</span><span class="sxs-lookup"><span data-stu-id="6bf8c-142">Creating, selecting, renaming, and removing contexts</span></span>

<span data-ttu-id="6bf8c-143">Környezetek létrehozásához be kell jelentkeznie az Azure-ba.</span><span class="sxs-lookup"><span data-stu-id="6bf8c-143">To create a context, you must be signed in to Azure.</span></span> <span data-ttu-id="6bf8c-144">Az `Connect-AzAccount` parancsmag (vagy az aliasa, a `Login-AzAccount` parancsmag) beállítja az Azure PowerShell-parancsmagok által használt alapértelmezett környezetet, valamint lehetővé teszi a bejelentkezési hitelesítő adatai számára engedélyezett bérlők vagy előfizetések elérését.</span><span class="sxs-lookup"><span data-stu-id="6bf8c-144">The `Connect-AzAccount` cmdlet (or its alias, `Login-AzAccount`) sets the default context used by Azure PowerShell cmdlets, and allows you to access any tenants or subscriptions allowed by your credentials.</span></span>

<span data-ttu-id="6bf8c-145">A bejelentkezés után új környezet hozzáadásához használja a `Set-AzContext` parancsmagot (vagy az aliasát, a `Select-AzSubscription` parancsmagot).</span><span class="sxs-lookup"><span data-stu-id="6bf8c-145">To add a new context after sign-in, use `Set-AzContext` (or its alias, `Select-AzSubscription`).</span></span>

```azurepowershell-interactive
PS C:\> Set-AzContext -Subscription "Contoso Subscription 1" -Name "Contoso1"
```

<span data-ttu-id="6bf8c-146">Az előző példa hozzáad egy új környezetet, amely a „Contoso Subscription 1” nevű előfizetést célozza az aktuális hitelesítő adatokkal.</span><span class="sxs-lookup"><span data-stu-id="6bf8c-146">The previous example adds a new context targeting 'Contoso Subscription 1' using your current credentials.</span></span> <span data-ttu-id="6bf8c-147">Az új környezet neve „Contoso1”.</span><span class="sxs-lookup"><span data-stu-id="6bf8c-147">The new context is named 'Contoso1'.</span></span> <span data-ttu-id="6bf8c-148">Ha nem ad meg nevet a környezetnek, a rendszer egy alapértelmezett nevet ad a használt fiók- és előfizetés-azonosító alapján.</span><span class="sxs-lookup"><span data-stu-id="6bf8c-148">If you don't provide a name for the context, a default name, using the account ID and subscription ID is used.</span></span>

<span data-ttu-id="6bf8c-149">Meglévő környezetek átnevezéséhez használja a `Rename-AzContext` parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="6bf8c-149">To rename an existing context, use the `Rename-AzContext` cmdlet.</span></span> <span data-ttu-id="6bf8c-150">Például:</span><span class="sxs-lookup"><span data-stu-id="6bf8c-150">For example:</span></span>

```azurepowershell-interactive
PS C:\> Rename-AzContext '[user1@contoso.org; 123456-7890-1234-564321]` 'Contoso2'
```

<span data-ttu-id="6bf8c-151">A példa az automatikusan elnevezett `[user1@contoso.org; 123456-7890-1234-564321]` környezetet átnevezi az egyszerű „Contoso2” névre.</span><span class="sxs-lookup"><span data-stu-id="6bf8c-151">This example renames the context with automatic name `[user1@contoso.org; 123456-7890-1234-564321]` to the simple name 'Contoso2'.</span></span> <span data-ttu-id="6bf8c-152">A környezetek kezelésére szolgáló parancsmagok parancssori kiegészítés funkcióval rendelkeznek, így a beírásukkor gyorsan kiválasztható a környezet.</span><span class="sxs-lookup"><span data-stu-id="6bf8c-152">Cmdlets that manage contexts also use tab completion, allowing you to quickly select the context.</span></span>

<span data-ttu-id="6bf8c-153">A környezet a `Remove-AzContext` parancsmaggal távolítható el.</span><span class="sxs-lookup"><span data-stu-id="6bf8c-153">Finally, to remove a context, use the `Remove-AzContext` cmdlet.</span></span>  <span data-ttu-id="6bf8c-154">Például:</span><span class="sxs-lookup"><span data-stu-id="6bf8c-154">For example:</span></span>

```azurepowershell-interactive
PS C:\> Remove-AzContext Contoso2
```

<span data-ttu-id="6bf8c-155">Elfelejti a „Contoso2” nevű környezetet.</span><span class="sxs-lookup"><span data-stu-id="6bf8c-155">Forgets the context that was named 'Contoso2'.</span></span> <span data-ttu-id="6bf8c-156">A környezet a `Set-AzContext` parancsmaggal hozható újra létre</span><span class="sxs-lookup"><span data-stu-id="6bf8c-156">You can recreate this context using `Set-AzContext`</span></span>

## <a name="removing-credentials"></a><span data-ttu-id="6bf8c-157">Hitelesítő adatok eltávolítása</span><span class="sxs-lookup"><span data-stu-id="6bf8c-157">Removing credentials</span></span>

<span data-ttu-id="6bf8c-158">Egy adott felhasználó vagy szolgáltatásnév összes hitelesítő adatát és társított környezetét a `Disconnect-AzAccount` (vagy más néven `Logout-AzAccount`) parancsmaggal távolíthatja el.</span><span class="sxs-lookup"><span data-stu-id="6bf8c-158">You can remove all credentials and associated contexts for a user or service principal using `Disconnect-AzAccount` (also known as `Logout-AzAccount`).</span></span> <span data-ttu-id="6bf8c-159">Paraméterek nélkül a `Disconnect-AzAccount` parancsmag az aktuális környezetben bejelentkezett felhasználó vagy szolgáltatásnév összes társított hitelesítő adatát és környezetét eltávolítja.</span><span class="sxs-lookup"><span data-stu-id="6bf8c-159">When executed without parameters, the `Disconnect-AzAccount` cmdlet removes all credentials and contexts associated with the User or Service Principal in the current context.</span></span> <span data-ttu-id="6bf8c-160">A parancsmagnak átadható egy felhasználónév, egyszerű szolgáltatásnév vagy egy környezet is, ha egy adott szolgáltatást kíván megcélozni.</span><span class="sxs-lookup"><span data-stu-id="6bf8c-160">You may pass in a Username, Service Principal Name, or context to target a particular principal.</span></span>

```azurepowershell-interactive
Disconnect-AzAccount user1@contoso.org
```

## <a name="using-context-scopes"></a><span data-ttu-id="6bf8c-161">Környezeti hatókörök használata</span><span class="sxs-lookup"><span data-stu-id="6bf8c-161">Using context scopes</span></span>

<span data-ttu-id="6bf8c-162">Előfordulhat, hogy úgy szeretné kiválasztani, módosítani vagy eltávolítani egy PowerShell-munkamenet valamely környezetét, hogy a többi munkamenetet ne érintse a módosítás.</span><span class="sxs-lookup"><span data-stu-id="6bf8c-162">Occasionally, you may want to select, change, or remove a context in a PowerShell session without impacting other sessions.</span></span> <span data-ttu-id="6bf8c-163">A környezeti parancsmagok alapértelmezett viselkedésének módosításához használja a `Scope` paramétert.</span><span class="sxs-lookup"><span data-stu-id="6bf8c-163">To change the default behavior of context cmdlets, use the `Scope` parameter.</span></span> <span data-ttu-id="6bf8c-164">A `Process` hatókör felülírja az alapértelmezett viselkedést, hogy csak az aktuális munkamenetre vonatkozzon.</span><span class="sxs-lookup"><span data-stu-id="6bf8c-164">The `Process` scope overrides the default behavior by making it apply only for the current session.</span></span> <span data-ttu-id="6bf8c-165">A `CurrentUser` hatókör ezzel szemben nemcsak az aktuális, hanem minden munkamenetben módosítja a környezetet.</span><span class="sxs-lookup"><span data-stu-id="6bf8c-165">Conversely `CurrentUser` scope changes the context in all sessions, instead of just the current session.</span></span>

<span data-ttu-id="6bf8c-166">Ha például anélkül szeretné módosítani az aktuális PowerShell-munkamenet alapértelmezett környezetét, hogy a módosítás a többi ablakot vagy a munkamenet következő megnyitásakor használt környezetet is érintené, használja a következő parancsmagot:</span><span class="sxs-lookup"><span data-stu-id="6bf8c-166">As an example, to change the default context in the current PowerShell session without impacting other windows, or the context used the next time a session is opened, use:</span></span>

```azurepowershell-interactive
PS C:\> Select-AzContext Contoso1 -Scope Process
```

## <a name="how-the-context-autosave-setting-is-remembered"></a><span data-ttu-id="6bf8c-167">A környezet automatikus mentési beállításainak megőrzése</span><span class="sxs-lookup"><span data-stu-id="6bf8c-167">How the context autosave setting is remembered</span></span>

<span data-ttu-id="6bf8c-168">A rendszer a felhasználó Azure PowerShell-könyvtárába (`$env:USERPROFILE\.Azure` Windows rendszeren és `$HOME/.Azure` más platformokon) menti a környezet automatikus mentési beállításait.</span><span class="sxs-lookup"><span data-stu-id="6bf8c-168">The context AutoSave setting is saved to the user Azure PowerShell directory (`$env:USERPROFILE\.Azure` on Windows, and `$HOME/.Azure` on other platforms).</span></span> <span data-ttu-id="6bf8c-169">Előfordulhat, hogy egyes számítógépfiókok nem rendelkeznek hozzáféréshez ehhez a könyvtárhoz.</span><span class="sxs-lookup"><span data-stu-id="6bf8c-169">Some kinds of computer accounts may not have access to this directory.</span></span> <span data-ttu-id="6bf8c-170">Ilyen esetekben használhatja a következő környezeti változót:</span><span class="sxs-lookup"><span data-stu-id="6bf8c-170">For such scenarios, you can use the environment variable</span></span>

```azurepowershell-interactive
$env:AzureRmContextAutoSave="true" | "false"
```

<span data-ttu-id="6bf8c-171">Ha a változó értéke „true”, a rendszer automatikusan menti a környezetet.</span><span class="sxs-lookup"><span data-stu-id="6bf8c-171">When set to 'true', the context is automatically saved.</span></span> <span data-ttu-id="6bf8c-172">Ha az érték „false”, a rendszer nem menti a környezetet.</span><span class="sxs-lookup"><span data-stu-id="6bf8c-172">If set to 'false', the context isn't saved.</span></span>

## <a name="context-management-cmdlets"></a><span data-ttu-id="6bf8c-173">Környezet kezelésének parancsmagjai</span><span class="sxs-lookup"><span data-stu-id="6bf8c-173">Context management cmdlets</span></span>

- <span data-ttu-id="6bf8c-174">[Enable-AzContextAutosave][enable] – A környezet mentésének engedélyezése a PowerShell-munkamenetek között.</span><span class="sxs-lookup"><span data-stu-id="6bf8c-174">[Enable-AzContextAutosave][enable] - Allow saving the context between powershell sessions.</span></span>
  <span data-ttu-id="6bf8c-175">Minden változás módosítja a globális környezetet.</span><span class="sxs-lookup"><span data-stu-id="6bf8c-175">Any changes alter the global context.</span></span>
- <span data-ttu-id="6bf8c-176">[Disable-AzContextAutosave][disable] – A környezet automatikus mentésének letiltása.</span><span class="sxs-lookup"><span data-stu-id="6bf8c-176">[Disable-AzContextAutosave][disable] - Turn off autosaving the context.</span></span> <span data-ttu-id="6bf8c-177">Minden egyes új PowerShell-munkamenetnek újra be kell jelentkeznie.</span><span class="sxs-lookup"><span data-stu-id="6bf8c-177">Each new PowerShell session is required to sign in again.</span></span>
- <span data-ttu-id="6bf8c-178">[Select-AzContext][select] – Az alapértelmezett környezet kiválasztása.</span><span class="sxs-lookup"><span data-stu-id="6bf8c-178">[Select-AzContext][select] - Select a context as the default.</span></span> <span data-ttu-id="6bf8c-179">Az összes parancsmag ennek a környezetnek a hitelesítő adatait használja.</span><span class="sxs-lookup"><span data-stu-id="6bf8c-179">All cmdlets use the credentials in this context for authentication.</span></span>
- <span data-ttu-id="6bf8c-180">[Disconnect-AzAccount][remove-cred] – Egy fiókhoz tartozó összes hitelesítő adat és környezet eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="6bf8c-180">[Disconnect-AzAccount][remove-cred] - Remove all credentials and contexts associated with an account.</span></span>
- <span data-ttu-id="6bf8c-181">[Remove-AzContext][remove-context] – Egy nevesített környezet eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="6bf8c-181">[Remove-AzContext][remove-context] - Remove a named context.</span></span>
- <span data-ttu-id="6bf8c-182">[Rename-AzContext][rename] – Meglévő környezet átnevezése.</span><span class="sxs-lookup"><span data-stu-id="6bf8c-182">[Rename-AzContext][rename] - Rename an existing context.</span></span>
- <span data-ttu-id="6bf8c-183">[Add-AzAccount][login] – Lehetővé teszi a bejelentkezés hatókörének beállítását a folyamatra vagy az aktuális felhasználóra.</span><span class="sxs-lookup"><span data-stu-id="6bf8c-183">[Add-AzAccount][login] - Allow scoping of the sign-in to the process or the current user.</span></span>
  <span data-ttu-id="6bf8c-184">Lehetővé teszi az alapértelmezett környezet elnevezését a bejelentkezés után.</span><span class="sxs-lookup"><span data-stu-id="6bf8c-184">Allow naming the default context after authentication.</span></span>
- <span data-ttu-id="6bf8c-185">[Import-AzContext][import] – Lehetővé teszi a bejelentkezés hatókörének beállítását a folyamatra vagy az aktuális felhasználóra.</span><span class="sxs-lookup"><span data-stu-id="6bf8c-185">[Import-AzContext][import] - Allow scoping of the sign-in to the process or the current user.</span></span>
- <span data-ttu-id="6bf8c-186">[Set-AzContext][set-context] – Lehetővé teszi meglévő nevesített környezetek kiválasztását, valamint a hatókör módosítását a folyamatra vagy az aktuális felhasználóra.</span><span class="sxs-lookup"><span data-stu-id="6bf8c-186">[Set-AzContext][set-context] - Allow selection of existing named contexts, and scope changes to the process or current user.</span></span>

<!-- Hyperlinks -->
[enable]: /powershell/module/az.accounts/Enable-AzureRmContextAutosave
[disable]: /powershell/module/az.accounts/Disable-AzContextAutosave
[select]: /powershell/module/az.accounts/Select-AzContext
[remove-cred]: /powershell/module/az.accounts/Disconnect-AzAccount
[remove-context]: /powershell/module/az.accounts/Remove-AzContext
[rename]: /powershell/module/az.accounts/Rename-AzContext

<!-- Updated cmdlets -->
[login]: /powershell/module/az.accounts/Connect-AzAccount
[import]:  /powershell/module/az.accounts/Import-AzContext
[set-context]: /powershell/module/az.accounts/Set-AzContext
