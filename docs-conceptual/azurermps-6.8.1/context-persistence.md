---
title: Felhasználói hitelesítő adatok megőrzése a PowerShell-munkamenetek között
description: A cikkből megismerheti, hogyan használhatók fel újra az Azure-beli hitelesítő és egyéb adatok több PowerShell-munkamenet során.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 09/09/2018
ms.openlocfilehash: 9867efc991f4a9efe880c0f449d9d2be1cddf8ef
ms.sourcegitcommit: 3a02e0c85c83de873981dd392500bc82c1cf9286
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 09/24/2018
ms.locfileid: "46559895"
---
# <a name="persist-user-credentials-across-powershell-sessions"></a><span data-ttu-id="27848-103">Felhasználói hitelesítő adatok megőrzése a PowerShell-munkamenetek között</span><span class="sxs-lookup"><span data-stu-id="27848-103">Persist user credentials across PowerShell sessions</span></span>

<span data-ttu-id="27848-104">Az Azure PowerShell új, **Azure-környezet automatikus mentése** nevű funkciója a következő szolgáltatásokat nyújtja:</span><span class="sxs-lookup"><span data-stu-id="27848-104">Azure PowerShell offers a feature called **Azure Context Autosave**, which gives the following features:</span></span>

- <span data-ttu-id="27848-105">A bejelentkezési adatok megőrzése és ismételt használata az új PowerShell-munkamenetekben.</span><span class="sxs-lookup"><span data-stu-id="27848-105">Retention of sign-in information for reuse in new PowerShell sessions.</span></span>
- <span data-ttu-id="27848-106">A háttérfeladatok egyszerűbb használata a hosszú ideig futó parancsmagok végrehajtásához.</span><span class="sxs-lookup"><span data-stu-id="27848-106">Easier use of background tasks for executing long-running cmdlets.</span></span>
- <span data-ttu-id="27848-107">Váltás a fiókok, előfizetések és környezet között külön bejelentkezés nélkül.</span><span class="sxs-lookup"><span data-stu-id="27848-107">Switch between accounts, subscriptions, and environments without a separate sign-in.</span></span>
- <span data-ttu-id="27848-108">Feladatok egyidejű végrehajtása több bejelentkezés és előfizetés használatával ugyanabból a PowerShell-munkamenetből.</span><span class="sxs-lookup"><span data-stu-id="27848-108">Execution of tasks using different credentials and subscriptions, simultaneously, from the same PowerShell session.</span></span>

## <a name="azure-contexts-defined"></a><span data-ttu-id="27848-109">Az Azure-környezetek</span><span class="sxs-lookup"><span data-stu-id="27848-109">Azure contexts defined</span></span>

<span data-ttu-id="27848-110">Az *Azure-környezet* az Azure PowerShell-parancsmagok célját meghatározó adatok halmaza.</span><span class="sxs-lookup"><span data-stu-id="27848-110">An *Azure context* is a set of information that defines the target of Azure PowerShell cmdlets.</span></span> <span data-ttu-id="27848-111">A környezet öt részből áll:</span><span class="sxs-lookup"><span data-stu-id="27848-111">The context consists of five parts:</span></span>

- <span data-ttu-id="27848-112">A *Fiók* – Az Azure-beli kommunikáció hitelesítéséhez használt felhasználónév vagy szolgáltatásnév</span><span class="sxs-lookup"><span data-stu-id="27848-112">An *Account* - the UserName or Service Principal used to authenticate communications with Azure</span></span>
- <span data-ttu-id="27848-113">Az *előfizetés* – Az adott erőforrásokat tartalmazó Azure-előfizetés, amelyre a műveletek irányulnak.</span><span class="sxs-lookup"><span data-stu-id="27848-113">A *Subscription* - The Azure Subscription with the Resources being acted upon.</span></span>
- <span data-ttu-id="27848-114">A *bérlő* – Az előfizetést tartalmazó Azure Active Directory-bérlő.</span><span class="sxs-lookup"><span data-stu-id="27848-114">A *Tenant* - The Azure Active Directory tenant that contains your subscription.</span></span> <span data-ttu-id="27848-115">A bérlők a szolgáltatásnévvel való hitelesítés során fontosabbak.</span><span class="sxs-lookup"><span data-stu-id="27848-115">Tenants are more important to ServicePrincipal authentication.</span></span>
- <span data-ttu-id="27848-116">A *környezet* – A célzott Azure-felhő, általában az Azure globális felhője.</span><span class="sxs-lookup"><span data-stu-id="27848-116">An *Environment* - The particular Azure Cloud being targeted, usually the Azure global Cloud.</span></span>
  <span data-ttu-id="27848-117">A környezetbeállításban azonban megadhat országos, kormányzati és helyszíni (Azure Stack) felhőket is.</span><span class="sxs-lookup"><span data-stu-id="27848-117">However, the environment setting allows you to target National, Government, and on-premises (Azure Stack) clouds as well.</span></span>
- <span data-ttu-id="27848-118">A *hitelesítő adatok* – Az Azure által az identitás és az Azure-erőforrások hozzáférési jogosultságának ellenőrzéséhez használt adatok.</span><span class="sxs-lookup"><span data-stu-id="27848-118">*Credentials* - The information used by Azure to verify your identity and confirm your authorization to access resources in Azure</span></span>

<span data-ttu-id="27848-119">A korábbi kiadásokban az új PowerShell-munkamenetek megnyitásakor minden egyes alkalommal létre kellett hozni egy Azure-környezetet.</span><span class="sxs-lookup"><span data-stu-id="27848-119">In previous releases, an Azure Context had to be created each time you opened a new PowerShell session.</span></span> <span data-ttu-id="27848-120">Az Azure PowerShell 4.4.0-s verziójától kezdve azonban új PowerShell-munkamenet megnyitásakor beállítható az Azure-környezet automatikus mentése.</span><span class="sxs-lookup"><span data-stu-id="27848-120">Beginning with Azure PowerShell v4.4.0, Azure Contexts can automatically be saved whenever opening a new PowerShell session.</span></span>

## <a name="automatically-save-the-context-for-the-next-sign-in"></a><span data-ttu-id="27848-121">A környezet automatikus mentése a következő bejelentkezéshez</span><span class="sxs-lookup"><span data-stu-id="27848-121">Automatically save the context for the next sign-in</span></span>

<span data-ttu-id="27848-122">Az Azure PowerShell a 6.3.0-s verziótól kezdve automatikusan megőrzi a környezet adatait a munkamenetek között.</span><span class="sxs-lookup"><span data-stu-id="27848-122">In versions 6.3.0 and later, Azure PowerShell retains your context information automatically between sessions.</span></span> <span data-ttu-id="27848-123">Ha szeretné beállítani, hogy a PowerShell elfelejtse a környezetet és a hitelesítő adatokat, használja a `Disable-AzureRmContextAutoSave` parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="27848-123">To set PowerShell to forget your context and credentials, use `Disable-AzureRmContextAutoSave`.</span></span> <span data-ttu-id="27848-124">Ekkor minden alkalommal újra be kell majd jelentkeznie az Azure-ba, amikor megnyit egy PowerShell-munkamenetet.</span><span class="sxs-lookup"><span data-stu-id="27848-124">You'll need to sign in to Azure every time you open a PowerShell session.</span></span>

<span data-ttu-id="27848-125">Ha szeretné engedélyezni, hogy az Azure PowerShell megjegyezze a környezet adatait a PowerShell-munkamenetek bezárásakor, használja az `Enable-AzureRmContextAutosave` parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="27848-125">To allow Azure PowerShell to remember your context after the PowerShell session is closed, use `Enable-AzureRmContextAutosave`.</span></span> <span data-ttu-id="27848-126">A rendszer automatikusan menti a környezet adatait és a hitelesítő adatokat egy speciális rejtett mappába a felhasználó könyvtárában (`%AppData%\Roaming\Windows Azure PowerShell`).</span><span class="sxs-lookup"><span data-stu-id="27848-126">Context and credential information are automatically saved in a special hidden folder in your user directory (`%AppData%\Roaming\Windows Azure PowerShell`).</span></span>
<span data-ttu-id="27848-127">Minden egyes új PowerShell-munkamenet az utolsó munkamenet során használt környezetre irányul.</span><span class="sxs-lookup"><span data-stu-id="27848-127">Each new PowerShell session targets the context used in your last session.</span></span>

<span data-ttu-id="27848-128">Az Azure-környezetek kezeléséhez használt parancsmagokkal pontosan szabályozható a működés.</span><span class="sxs-lookup"><span data-stu-id="27848-128">The cmdlets that allow you to manage Azure contexts also allow you fine grained control.</span></span> <span data-ttu-id="27848-129">Például megadhatja, hogy a módosítások csak az aktuális PowerShell-munkamenetre (`Process` hatókör) vagy minden PowerShell-munkamenetre (`CurrentUser` hatókör) érvényesek legyenek.</span><span class="sxs-lookup"><span data-stu-id="27848-129">If you want changes to apply only to the current PowerShell session (`Process` scope) or every PowerShell session (`CurrentUser` scope).</span></span> <span data-ttu-id="27848-130">Ezeket a beállításokat a részletesebben a [Környezeti hatókörök használata](#Using-Context-Scopes) című szakasz tárgyalja.</span><span class="sxs-lookup"><span data-stu-id="27848-130">These options are discussed in mode detail in [Using Context Scopes](#Using-Context-Scopes).</span></span>

## <a name="running-azure-powershell-cmdlets-as-background-jobs"></a><span data-ttu-id="27848-131">Azure PowerShell-parancsmagok futtatása háttérfeladatként</span><span class="sxs-lookup"><span data-stu-id="27848-131">Running Azure PowerShell cmdlets as background jobs</span></span>

<span data-ttu-id="27848-132">Az **Azure-környezet automatikus mentése** funkcióval megoszthatja a környezetet a PowerShell-háttérfeladatokkal.</span><span class="sxs-lookup"><span data-stu-id="27848-132">The **Azure Context Autosave** feature also allows you to share you context with PowerShell background jobs.</span></span> <span data-ttu-id="27848-133">A PowerShell segítségével a hosszú lefutású feladatokat indíthatja és monitorozhatja háttérfeladatokként is, így nem kell megvárnia, amíg ezek befejeződnek.</span><span class="sxs-lookup"><span data-stu-id="27848-133">PowerShell allows you to start and monitor long-executing tasks as background jobs without having to wait for the tasks to complete.</span></span> <span data-ttu-id="27848-134">A hitelesítő adatokat kétféleképpen oszthatja meg a háttérfeladatokkal:</span><span class="sxs-lookup"><span data-stu-id="27848-134">You can share credentials with background jobs in two different ways:</span></span>

- <span data-ttu-id="27848-135">A környezet átadása argumentumként</span><span class="sxs-lookup"><span data-stu-id="27848-135">Passing the context as an argument</span></span>

  <span data-ttu-id="27848-136">A legtöbb AzureRM-parancsmagba a környezet átadható a parancsmag paramétereként.</span><span class="sxs-lookup"><span data-stu-id="27848-136">Most AzureRM cmdlets allow you to pass the context as a parameter to the cmdlet.</span></span> <span data-ttu-id="27848-137">A környezet a háttérfeladat számára az alábbi példában látható módon adható át:</span><span class="sxs-lookup"><span data-stu-id="27848-137">You can pass a context to a background job as shown in the following example:</span></span>

  ```powershell
  PS C:\> $job = Start-Job { param ($ctx) New-AzureRmVm -AzureRmContext $ctx [... Additional parameters ...]} -ArgumentList (Get-AzureRmContext)
  ```

- <span data-ttu-id="27848-138">Az alapértelmezett környezet használata működő automatikus mentés mellett</span><span class="sxs-lookup"><span data-stu-id="27848-138">Using the default context with Autosave enabled</span></span>

  <span data-ttu-id="27848-139">Ha engedélyezte a **Környezet automatikus mentése** funkciót, a háttérfeladatok automatikusan az alapértelmezett mentett környezetet használják.</span><span class="sxs-lookup"><span data-stu-id="27848-139">If you have enabled **Context Autosave**, background jobs automatically use the default saved context.</span></span>

  ```powershell
  PS C:\> $job = Start-Job { New-AzureRmVm [... Additional parameters ...]}
  ```

<span data-ttu-id="27848-140">Ha tájékozódni szeretne egy háttérfeladat kimeneteléről, a `Get-Job` parancsmaggal ellenőrizheti le a feladat állapotát, és a `Wait-Job` parancsmaggal várhatja meg a feladat befejezését.</span><span class="sxs-lookup"><span data-stu-id="27848-140">When you need to know the outcome of the background task, use `Get-Job` to check the job status and `Wait-Job` to wait for the Job to complete.</span></span> <span data-ttu-id="27848-141">A `Receive-Job` parancsmaggal rögzítheti és jelenítheti meg a háttérfeladat kimenetét.</span><span class="sxs-lookup"><span data-stu-id="27848-141">Use `Receive-Job` to capture or display the output of the background job.</span></span> <span data-ttu-id="27848-142">További információkért lásd a [feladatokat ismertető szakaszt](/powershell/module/microsoft.powershell.core/about/about_jobs).</span><span class="sxs-lookup"><span data-stu-id="27848-142">For more information, see [about_Jobs](/powershell/module/microsoft.powershell.core/about/about_jobs).</span></span>

## <a name="creating-selecting-renaming-and-removing-contexts"></a><span data-ttu-id="27848-143">Környezetek létrehozása, kiválasztása, átnevezése és eltávolítása</span><span class="sxs-lookup"><span data-stu-id="27848-143">Creating, selecting, renaming, and removing contexts</span></span>

<span data-ttu-id="27848-144">Környezetek létrehozásához be kell jelentkeznie az Azure-ba.</span><span class="sxs-lookup"><span data-stu-id="27848-144">To create a context, you must be signed in to Azure.</span></span> <span data-ttu-id="27848-145">Az `Connect-AzureRmAccount` parancsmag (vagy az aliasa, a `Login-AzureRmAccount` parancsmag) beállítja az Azure PowerShell-parancsmagok által használt alapértelmezett környezetet, valamint lehetővé teszi a bejelentkezési hitelesítő adatai számára engedélyezett bérlők vagy előfizetések elérését.</span><span class="sxs-lookup"><span data-stu-id="27848-145">The `Connect-AzureRmAccount` cmdlet (or its alias, `Login-AzureRmAccount`) sets the default context used by Azure PowerShell cmdlets, and allows you to access any tenants or subscriptions allowed by your credentials.</span></span>

<span data-ttu-id="27848-146">A bejelentkezés után új környezet hozzáadásához használja a `Set-AzureRmContext` parancsmagot (vagy az aliasát, a `Select-AzureRmSubscription` parancsmagot).</span><span class="sxs-lookup"><span data-stu-id="27848-146">To add a new context after sign-in, use `Set-AzureRmContext` (or its alias, `Select-AzureRmSubscription`).</span></span>

```azurepowershell-interactive
PS C:\> Set-AzureRMContext -Subscription "Contoso Subscription 1" -Name "Contoso1"
```

<span data-ttu-id="27848-147">Az előző példa hozzáad egy új környezetet, amely a „Contoso Subscription 1” nevű előfizetést célozza az aktuális hitelesítő adatokkal.</span><span class="sxs-lookup"><span data-stu-id="27848-147">The previous example adds a new context targeting 'Contoso Subscription 1' using your current credentials.</span></span> <span data-ttu-id="27848-148">Az új környezet neve „Contoso1”.</span><span class="sxs-lookup"><span data-stu-id="27848-148">The new context is named 'Contoso1'.</span></span> <span data-ttu-id="27848-149">Ha nem ad meg nevet a környezetnek, a rendszer egy alapértelmezett nevet ad a használt fiók- és előfizetés-azonosító alapján.</span><span class="sxs-lookup"><span data-stu-id="27848-149">If you don't provide a name for the context, a default name, using the account ID and subscription ID is used.</span></span>

<span data-ttu-id="27848-150">Meglévő környezetek átnevezéséhez használja a `Rename-AzureRmContext` parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="27848-150">To rename an existing context, use the `Rename-AzureRmContext` cmdlet.</span></span> <span data-ttu-id="27848-151">Például:</span><span class="sxs-lookup"><span data-stu-id="27848-151">For example:</span></span>

```azurepowershell-interactive
PS C:\> Rename-AzureRmContext '[user1@contoso.org; 123456-7890-1234-564321]` 'Contoso2'
```

<span data-ttu-id="27848-152">A példa az automatikusan elnevezett `[user1@contoso.org; 123456-7890-1234-564321]` környezetet átnevezi az egyszerű „Contoso2” névre.</span><span class="sxs-lookup"><span data-stu-id="27848-152">This example renames the context with automatic name `[user1@contoso.org; 123456-7890-1234-564321]` to the simple name 'Contoso2'.</span></span> <span data-ttu-id="27848-153">A környezetek kezelésére szolgáló parancsmagok parancssori kiegészítés funkcióval rendelkeznek, így a beírásukkor gyorsan kiválasztható a környezet.</span><span class="sxs-lookup"><span data-stu-id="27848-153">Cmdlets that manage contexts also use tab completion, allowing you to quickly select the context.</span></span>

<span data-ttu-id="27848-154">A környezet a `Remove-AzureRmContext` parancsmaggal távolítható el.</span><span class="sxs-lookup"><span data-stu-id="27848-154">Finally, to remove a context, use the `Remove-AzureRmContext` cmdlet.</span></span>  <span data-ttu-id="27848-155">Például:</span><span class="sxs-lookup"><span data-stu-id="27848-155">For example:</span></span>

```azurepowershell-interactive
PS C:\> Remove-AzureRmContext Contoso2
```

<span data-ttu-id="27848-156">Elfelejti a „Contoso2” nevű környezetet.</span><span class="sxs-lookup"><span data-stu-id="27848-156">Forgets the context that was named 'Contoso2'.</span></span> <span data-ttu-id="27848-157">A környezet a `Set-AzureRmContext` parancsmaggal hozható újra létre</span><span class="sxs-lookup"><span data-stu-id="27848-157">You can recreate this context using `Set-AzureRmContext`</span></span>

## <a name="removing-credentials"></a><span data-ttu-id="27848-158">Hitelesítő adatok eltávolítása</span><span class="sxs-lookup"><span data-stu-id="27848-158">Removing credentials</span></span>

<span data-ttu-id="27848-159">Egy adott felhasználó vagy szolgáltatásnév összes hitelesítő adatát és társított környezetét a `Disconnect-AzureRmAccount` (vagy más néven `Logout-AzureRmAccount`) parancsmaggal távolíthatja el.</span><span class="sxs-lookup"><span data-stu-id="27848-159">You can remove all credentials and associated contexts for a user or service principal using `Disconnect-AzureRmAccount` (also known as `Logout-AzureRmAccount`).</span></span> <span data-ttu-id="27848-160">Paraméterek nélkül a `Disconnect-AzureRmAccount` parancsmag az aktuális környezetben bejelentkezett felhasználó vagy szolgáltatásnév összes társított hitelesítő adatát és környezetét eltávolítja.</span><span class="sxs-lookup"><span data-stu-id="27848-160">When executed without parameters, the `Disconnect-AzureRmAccount` cmdlet removes all credentials and contexts associated with the User or Service Principal in the current context.</span></span> <span data-ttu-id="27848-161">A parancsmagnak átadható egy felhasználónév, egyszerű szolgáltatásnév vagy egy környezet is, ha egy adott szolgáltatást kíván megcélozni.</span><span class="sxs-lookup"><span data-stu-id="27848-161">You may pass in a Username, Service Principal Name, or context to target a particular principal.</span></span>

```azurepowershell-interactive
Disconnect-AzureRmAccount user1@contoso.org
```

## <a name="using-context-scopes"></a><span data-ttu-id="27848-162">Környezeti hatókörök használata</span><span class="sxs-lookup"><span data-stu-id="27848-162">Using context scopes</span></span>

<span data-ttu-id="27848-163">Előfordulhat, hogy úgy szeretné kiválasztani, módosítani vagy eltávolítani egy PowerShell-munkamenet valamely környezetét, hogy a többi munkamenetet ne érintse a módosítás.</span><span class="sxs-lookup"><span data-stu-id="27848-163">Occasionally, you may want to select, change, or remove a context in a PowerShell session without impacting other sessions.</span></span> <span data-ttu-id="27848-164">A környezeti parancsmagok alapértelmezett viselkedésének módosításához használja a `Scope` paramétert.</span><span class="sxs-lookup"><span data-stu-id="27848-164">To change the default behavior of context cmdlets, use the `Scope` parameter.</span></span> <span data-ttu-id="27848-165">A `Process` hatókör felülírja az alapértelmezett viselkedést, hogy csak az aktuális munkamenetre vonatkozzon.</span><span class="sxs-lookup"><span data-stu-id="27848-165">The `Process` scope overrides the default behavior by making it apply only for the current session.</span></span> <span data-ttu-id="27848-166">A `CurrentUser` hatókör ezzel szemben nemcsak az aktuális, hanem minden munkamenetben módosítja a környezetet.</span><span class="sxs-lookup"><span data-stu-id="27848-166">Conversely `CurrentUser` scope changes the context in all sessions, instead of just the current session.</span></span>

<span data-ttu-id="27848-167">Ha például anélkül szeretné módosítani az aktuális PowerShell-munkamenet alapértelmezett környezetét, hogy a módosítás a többi ablakot vagy a munkamenet következő megnyitásakor használt környezetet is érintené, használja a következő parancsmagot:</span><span class="sxs-lookup"><span data-stu-id="27848-167">As an example, to change the default context in the current PowerShell session without impacting other windows, or the context used the next time a session is opened, use:</span></span>

```azurepowershell-interactive
PS C:\> Select-AzureRmContext Contoso1 -Scope Process
```

## <a name="how-the-context-autosave-setting-is-remembered"></a><span data-ttu-id="27848-168">A környezet automatikus mentési beállításainak megőrzése</span><span class="sxs-lookup"><span data-stu-id="27848-168">How the context autosave setting is remembered</span></span>

<span data-ttu-id="27848-169">A rendszer a felhasználó Azure PowerShell-könyvtárába (`%AppData%\Roaming\Windows Azure PowerShell`) menti a környezet automatikus mentési beállításait.</span><span class="sxs-lookup"><span data-stu-id="27848-169">The context AutoSave setting is saved to the user Azure PowerShell directory (`%AppData%\Roaming\Windows Azure PowerShell`).</span></span> <span data-ttu-id="27848-170">Előfordulhat, hogy egyes számítógépfiókok nem rendelkeznek hozzáféréshez ehhez a könyvtárhoz.</span><span class="sxs-lookup"><span data-stu-id="27848-170">Some kinds of computer accounts may not have access to this directory.</span></span> <span data-ttu-id="27848-171">Ilyen esetekben használhatja a következő környezeti változót:</span><span class="sxs-lookup"><span data-stu-id="27848-171">For such scenarios, you can use the environment variable</span></span>

```azurepowershell-interactive
$env:AzureRmContextAutoSave="true" | "false"
```

<span data-ttu-id="27848-172">Ha a változó értéke „true”, a rendszer automatikusan menti a környezetet.</span><span class="sxs-lookup"><span data-stu-id="27848-172">When set to 'true', the context is automatically saved.</span></span> <span data-ttu-id="27848-173">Ha az érték „false”, a rendszer nem menti a környezetet.</span><span class="sxs-lookup"><span data-stu-id="27848-173">If set to 'false', the context isn't saved.</span></span>

## <a name="changes-to-the-azurermprofile-module"></a><span data-ttu-id="27848-174">Az AzureRM.Profile modul változásai</span><span class="sxs-lookup"><span data-stu-id="27848-174">Changes to the AzureRM.Profile module</span></span>

<span data-ttu-id="27848-175">Új parancsmagok a környezetek kezeléséhez</span><span class="sxs-lookup"><span data-stu-id="27848-175">New cmdlets for managing context</span></span>

- <span data-ttu-id="27848-176">[Enable-AzureRmContextAutosave][enable] – A környezet mentésének engedélyezése a PowerShell-munkamenetek között.</span><span class="sxs-lookup"><span data-stu-id="27848-176">[Enable-AzureRmContextAutosave][enable] - Allow saving the context between powershell sessions.</span></span>
  <span data-ttu-id="27848-177">Minden változás módosítja a globális környezetet.</span><span class="sxs-lookup"><span data-stu-id="27848-177">Any changes alter the global context.</span></span>
- <span data-ttu-id="27848-178">[Disable-AzureRmContextAutosave][disable] – A környezet automatikus mentésének letiltása.</span><span class="sxs-lookup"><span data-stu-id="27848-178">[Disable-AzureRmContextAutosave][disable] - Turn off autosaving the context.</span></span> <span data-ttu-id="27848-179">Minden egyes új PowerShell-munkamenetnek újra be kell jelentkeznie.</span><span class="sxs-lookup"><span data-stu-id="27848-179">Each new PowerShell session is required to sign in again.</span></span>
- <span data-ttu-id="27848-180">[Select-AzureRmContext][select] – Az alapértelmezett környezet kiválasztása.</span><span class="sxs-lookup"><span data-stu-id="27848-180">[Select-AzureRmContext][select] - Select a context as the default.</span></span> <span data-ttu-id="27848-181">Az összes parancsmag ennek a környezetnek a hitelesítő adatait használja.</span><span class="sxs-lookup"><span data-stu-id="27848-181">All cmdlets use the credentials in this context for authentication.</span></span>
- <span data-ttu-id="27848-182">[Disconnect-AzureRmAccount][remove-cred] – Egy fiókhoz tartozó összes hitelesítő adat és környezet eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="27848-182">[Disconnect-AzureRmAccount][remove-cred] - Remove all credentials and contexts associated with an account.</span></span>
- <span data-ttu-id="27848-183">[Remove-AzureRmContext][remove-context] – A megnevezett környezet eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="27848-183">[Remove-AzureRmContext][remove-context] - Remove a named context.</span></span>
- <span data-ttu-id="27848-184">[Rename-AzureRmContext][rename] – Meglévő környezet eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="27848-184">[Rename-AzureRmContext][rename] - Rename an existing context.</span></span>

<span data-ttu-id="27848-185">Meglévő profilparancsmagok változásai</span><span class="sxs-lookup"><span data-stu-id="27848-185">Changes to existing profile cmdlets</span></span>

- <span data-ttu-id="27848-186">[Add-AzureRmAccount][login] – Lehetővé teszi a bejelentkezés hatókörének beállítását a folyamatra vagy az aktuális felhasználóra.</span><span class="sxs-lookup"><span data-stu-id="27848-186">[Add-AzureRmAccount][login] - Allow scoping of the sign-in to the process or the current user.</span></span>
  <span data-ttu-id="27848-187">Lehetővé teszi az alapértelmezett környezet elnevezését a bejelentkezés után.</span><span class="sxs-lookup"><span data-stu-id="27848-187">Allow naming the default context after authentication.</span></span>
- <span data-ttu-id="27848-188">[Import-AzureRmContext][import] – Lehetővé teszi a bejelentkezés hatókörének beállítását a folyamatra vagy az aktuális felhasználóra.</span><span class="sxs-lookup"><span data-stu-id="27848-188">[Import-AzureRmContext][import] - Allow scoping of the sign-in to the process or the current user.</span></span>
- <span data-ttu-id="27848-189">[Set-AzureRmContext][set-context] – Lehetővé teszi meglévő megnevezett környezetek kiválasztását, valamint a hatókör beállítását a folyamatra vagy az aktuális felhasználóra.</span><span class="sxs-lookup"><span data-stu-id="27848-189">[Set-AzureRmContext][set-context] - Allow selection of existing named contexts, and scope changes to the process or current user.</span></span>

<!-- Hyperlinks -->
[enable]: /powershell/module/azurerm.profile/Enable-AzureRmContextAutosave
[disable]: /powershell/module/azurerm.profile/Disable-AzureRmContextAutosave
[select]: /powershell/module/azurerm.profile/Select-AzureRmContext
[remove-cred]: /powershell/module/azurerm.profile/Disconnect-AzureRmAccount
[remove-context]: /powershell/module/azurerm.profile/Remove-AzureRmContext
[rename]: /powershell/module/azurerm.profile/Rename-AzureRmContext

<!-- Updated cmdlets -->
[login]: /powershell/module/azurerm.profile/Connect-AzureRmAccount
[import]:  /powershell/module/azurerm.profile/Import-AzureRmContext
[set-context]: /powershell/module/azurerm.profile/Set-AzureRmContext
