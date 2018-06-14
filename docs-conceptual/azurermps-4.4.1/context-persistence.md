---
title: Felhasználói bejelentkezések megőrzése a PowerShell-munkamenetek között
description: A cikk az Azure PowerShell új funkcióit ismerteti, amellyel újra felhasználhatók a felhasználók hitelesítési és egyéb adatai az egymást követő PowerShell-munkamenetek során.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 08/31/2017
ms.openlocfilehash: d650cfaae580acd10b3ddb06edec9883f1a32844
ms.sourcegitcommit: c98e3a21037ebd82936828bcb544eed902b24212
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 06/08/2018
ms.locfileid: "34853967"
---
# <a name="persisting-user-logins-across-powershell-sessions"></a><span data-ttu-id="07100-103">Felhasználói bejelentkezések megőrzése a PowerShell-munkamenetek között</span><span class="sxs-lookup"><span data-stu-id="07100-103">Persisting user logins across PowerShell sessions</span></span>

<span data-ttu-id="07100-104">Az Azure PowerShell 2017. szeptemberi kiadásában az Azure Resource Manager parancsmagjaival bevezettünk egy új szolgáltatást, az **Azure-környezet automatikus mentését**.</span><span class="sxs-lookup"><span data-stu-id="07100-104">In the September 2017 release of Azure PowerShell, Azure Resource Manager cmdlets introduce a new feature, **Azure Context Autosave**.</span></span> <span data-ttu-id="07100-105">A szolgáltatás számos új felhasználói forgatókönyvet kínál, a következőket beleértve:</span><span class="sxs-lookup"><span data-stu-id="07100-105">This feature enables several new user scenarios, including:</span></span>

- <span data-ttu-id="07100-106">A bejelentkezési adatok megőrzése és ismételt használata az új PowerShell-munkamenetekben.</span><span class="sxs-lookup"><span data-stu-id="07100-106">Retention of login information for reuse in new PowerShell sessions.</span></span>
- <span data-ttu-id="07100-107">A háttérfeladatok egyszerűbb használata a hosszú ideig futó parancsmagok végrehajtásához.</span><span class="sxs-lookup"><span data-stu-id="07100-107">Easier use of background tasks for executing long-running cmdlets.</span></span>
- <span data-ttu-id="07100-108">Váltás a fiókok, előfizetések és környezet között külön bejelentkezés nélkül.</span><span class="sxs-lookup"><span data-stu-id="07100-108">Switch between accounts, subscriptions, and environments without a separate login.</span></span>
- <span data-ttu-id="07100-109">Feladatok egyidejű végrehajtása több bejelentkezés és előfizetés használatával ugyanabból a PowerShell-munkamenetből.</span><span class="sxs-lookup"><span data-stu-id="07100-109">Execution of tasks using different credentials and subscriptions, simultaneously, from the same PowerShell session.</span></span>

## <a name="azure-contexts-defined"></a><span data-ttu-id="07100-110">Az Azure-környezetek</span><span class="sxs-lookup"><span data-stu-id="07100-110">Azure contexts defined</span></span>

<span data-ttu-id="07100-111">Az *Azure-környezet* az Azure PowerShell-parancsmagok célját meghatározó adatok halmaza.</span><span class="sxs-lookup"><span data-stu-id="07100-111">An *Azure context* is a set of information that defines the target of Azure PowerShell cmdlets.</span></span> <span data-ttu-id="07100-112">A környezet öt részből áll:</span><span class="sxs-lookup"><span data-stu-id="07100-112">The context consists of five parts:</span></span>

- <span data-ttu-id="07100-113">A *Fiók* – Az Azure-beli kommunikáció hitelesítéséhez használt felhasználónév vagy szolgáltatásnév</span><span class="sxs-lookup"><span data-stu-id="07100-113">An *Account* - the UserName or Service Principal used to authenticate communications with Azure</span></span>
- <span data-ttu-id="07100-114">Az *előfizetés* – Az adott erőforrásokat tartalmazó Azure-előfizetés, amelyre a műveletek irányulnak.</span><span class="sxs-lookup"><span data-stu-id="07100-114">A *Subscription* - The Azure Subscription containing the Resources being acted upon.</span></span>
- <span data-ttu-id="07100-115">A *bérlő* – Az előfizetést tartalmazó Azure Active Directory-bérlő.</span><span class="sxs-lookup"><span data-stu-id="07100-115">A *Tenant* - The Azure Active Directory tenant that contains your subscription.</span></span> <span data-ttu-id="07100-116">A bérlők a szolgáltatásnévvel való hitelesítés során fontosabbak.</span><span class="sxs-lookup"><span data-stu-id="07100-116">Tenants are more important to ServicePrincipal authentication.</span></span>
- <span data-ttu-id="07100-117">A *környezet* – A célzott Azure-felhő, általában az Azure globális felhője.</span><span class="sxs-lookup"><span data-stu-id="07100-117">An *Environment* - The particular Azure Cloud being targeted, usually the Azure global Cloud.</span></span>
  <span data-ttu-id="07100-118">A környezetbeállításban azonban megadhat országos, kormányzati és helyszíni (Azure Stack) felhőket is.</span><span class="sxs-lookup"><span data-stu-id="07100-118">However, the environment setting allows you to target National, Government, and on-premises (Azure Stack) clouds as well.</span></span>
- <span data-ttu-id="07100-119">A *hitelesítő adatok* – Az Azure által az identitás és az Azure-erőforrások hozzáférési jogosultságának ellenőrzéséhez használt adatok.</span><span class="sxs-lookup"><span data-stu-id="07100-119">*Credentials* - The information used by Azure to verify your identity and ensure your authorization to access resources in Azure</span></span>

<span data-ttu-id="07100-120">A korábbi kiadásokban az új PowerShell-munkamenetek megnyitásakor minden egyes alkalommal létre kellett hozni az Azure-környezetet.</span><span class="sxs-lookup"><span data-stu-id="07100-120">In previous releases, your Azure Context had to be created each time you opened a new PowerShell session.</span></span> <span data-ttu-id="07100-121">Az Azure PowerShell 4.4.0-s verziójától azonban engedélyezheti az Azure-környezet automatikus mentését és egy új PowerShell-munkamenet megnyitásakor való újbóli használatát.</span><span class="sxs-lookup"><span data-stu-id="07100-121">Beginning with Azure PowerShell v4.4.0, you can enable the automatic saving and reuse of Azure Contexts whenever you open a new PowerShell session.</span></span>

## <a name="automatically-saving-the-context-for-the-next-login"></a><span data-ttu-id="07100-122">A környezet automatikus mentése a következő bejelentkezéshez</span><span class="sxs-lookup"><span data-stu-id="07100-122">Automatically saving the context for the next login</span></span>

<span data-ttu-id="07100-123">Az Azure PowerShell alapértelmezés szerint a munkamenetek bezárásakor elveti a környezet adatait.</span><span class="sxs-lookup"><span data-stu-id="07100-123">By default, Azure PowerShell discards your context information whenever you close the PowerShell session.</span></span>

<span data-ttu-id="07100-124">Ha szeretné engedélyezni, hogy az Azure PowerShell megjegyezze a környezet adatait a PowerShell-munkamenetek bezárásakor, használja az `Enable-AzureRmContextAutosave` parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="07100-124">To allow Azure PowerShell to remember your context after the PowerShell session is closed, use `Enable-AzureRmContextAutosave`.</span></span> <span data-ttu-id="07100-125">A rendszer automatikusan menti a környezet adatait és a hitelesítő adatokat egy speciális rejtett mappába a felhasználó könyvtárában (`%AppData%\Roaming\Windows Azure PowerShell`).</span><span class="sxs-lookup"><span data-stu-id="07100-125">Context and credential information are automatically saved in a special hidden folder in your user directory (`%AppData%\Roaming\Windows Azure PowerShell`).</span></span>
<span data-ttu-id="07100-126">Ezután minden egyes új PowerShell-munkamenet az utolsó munkamenet során használt környezetre irányul majd.</span><span class="sxs-lookup"><span data-stu-id="07100-126">Subsequently, each new PowerShell session targets the context used in your last session.</span></span>

<span data-ttu-id="07100-127">Ha szeretné beállítani, hogy a PowerShell elfelejtse a környezetet és a hitelesítő adatokat, használja a `Disable-AzureRmContextAutoSave` parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="07100-127">To set PowerShell to forget your context and credentials, use `Disable-AzureRmContextAutoSave`.</span></span> <span data-ttu-id="07100-128">Ekkor minden alkalommal újra be kell majd jelentkeznie az Azure-ba, amikor megnyit egy PowerShell-munkamenetet.</span><span class="sxs-lookup"><span data-stu-id="07100-128">You will need to log in to Azure every time you open a PowerShell session.</span></span>

<span data-ttu-id="07100-129">Az Azure-környezetek kezeléséhez használt parancsmagokkal pontosan szabályozható a működés.</span><span class="sxs-lookup"><span data-stu-id="07100-129">The cmdlets that allow you to manage Azure contexts also allow you fine grained control.</span></span> <span data-ttu-id="07100-130">Például megadhatja, hogy a módosítások csak az aktuális PowerShell-munkamenetre (`Process` hatókör) vagy minden PowerShell-munkamenetre (`CurrentUser` hatókör) érvényesek legyenek.</span><span class="sxs-lookup"><span data-stu-id="07100-130">If you want changes to apply only to the current PowerShell session (`Process` scope) or every PowerShell session (`CurrentUser` scope).</span></span> <span data-ttu-id="07100-131">Ezeket a beállításokat a részletesebben a [Környezeti hatókörök használata](#Using-Context-Scopes) című szakasz tárgyalja.</span><span class="sxs-lookup"><span data-stu-id="07100-131">These options are discussed in mode detail in [Using Context Scopes](#Using-Context-Scopes).</span></span>

## <a name="running-azure-powershell-cmdlets-as-background-jobs"></a><span data-ttu-id="07100-132">Azure PowerShell-parancsmagok futtatása háttérfeladatként</span><span class="sxs-lookup"><span data-stu-id="07100-132">Running Azure PowerShell cmdlets as background jobs</span></span>

<span data-ttu-id="07100-133">Az **Azure-környezet automatikus mentése** funkcióval megoszthatja a környezetet a PowerShell-háttérfeladatokkal.</span><span class="sxs-lookup"><span data-stu-id="07100-133">The **Azure Context Autosave** feature also allows you to share you context with PowerShell background jobs.</span></span> <span data-ttu-id="07100-134">A PowerShell segítségével a hosszú lefutású feladatokat indíthatja és monitorozhatja háttérfeladatokként is, így nem kell megvárnia, amíg ezek befejeződnek.</span><span class="sxs-lookup"><span data-stu-id="07100-134">PowerShell allows you to start and monitor long-executing tasks as background jobs without having to wait for the tasks to complete.</span></span> <span data-ttu-id="07100-135">A hitelesítő adatokat kétféleképpen oszthatja meg a háttérfeladatokkal:</span><span class="sxs-lookup"><span data-stu-id="07100-135">You can share credentials with background jobs in two different ways:</span></span>

- <span data-ttu-id="07100-136">A környezet átadása argumentumként</span><span class="sxs-lookup"><span data-stu-id="07100-136">Passing the context as an argument</span></span>

  <span data-ttu-id="07100-137">A legtöbb AzureRM-parancsmagba a környezet átadható a parancsmag paramétereként.</span><span class="sxs-lookup"><span data-stu-id="07100-137">Most AzureRM cmdlets allow you to pass the context as a parameter to the cmdlet.</span></span> <span data-ttu-id="07100-138">A környezet a háttérfeladat számára az alábbi példában látható módon adható át:</span><span class="sxs-lookup"><span data-stu-id="07100-138">You can pass a context to a background job as shown in the following example:</span></span>

  ```powershell
  PS C:\> $job = Start-Job { param ($ctx) New-AzureRmVm -AzureRmContext $ctx [... Additional parameters ...]} -ArgumentList (Get-AzureRmContext)
  ```

- <span data-ttu-id="07100-139">Az alapértelmezett környezet használata működő automatikus mentés mellett</span><span class="sxs-lookup"><span data-stu-id="07100-139">Using the default context with Autosave enabled</span></span>

  <span data-ttu-id="07100-140">Ha engedélyezte a **Környezet automatikus mentése** funkciót, a háttérfeladatok automatikusan az alapértelmezett mentett környezetet használják.</span><span class="sxs-lookup"><span data-stu-id="07100-140">If you have enabled **Context Autosave**, background jobs automatically use the default saved context.</span></span>

  ```powershell
  PS C:\> $job = Start-Job { New-AzureRmVm [... Additional parameters ...]}
  ```

<span data-ttu-id="07100-141">Ha tájékozódni szeretne egy háttérfeladat kimeneteléről, a `Get-Job` parancsmaggal ellenőrizheti le a feladat állapotát, és a `Wait-Job` parancsmaggal várhatja meg a feladat befejezését.</span><span class="sxs-lookup"><span data-stu-id="07100-141">When you need to know the outcome of the background task, use `Get-Job` to check the job status and `Wait-Job` to wait for the Job to complete.</span></span> <span data-ttu-id="07100-142">A `Receive-Job` parancsmaggal rögzítheti és jelenítheti meg a háttérfeladat kimenetét.</span><span class="sxs-lookup"><span data-stu-id="07100-142">Use `Receive-Job` to capture or display the output of the background job.</span></span> <span data-ttu-id="07100-143">További információkért lásd a [feladatokat ismertető szakaszt](/powershell/module/microsoft.powershell.core/about/about_jobs).</span><span class="sxs-lookup"><span data-stu-id="07100-143">For more information, see [about_Jobs](/powershell/module/microsoft.powershell.core/about/about_jobs).</span></span>

## <a name="creating-selecting-renaming-and-removing-contexts"></a><span data-ttu-id="07100-144">Környezetek létrehozása, kiválasztása, átnevezése és eltávolítása</span><span class="sxs-lookup"><span data-stu-id="07100-144">Creating, selecting, renaming, and removing contexts</span></span>

<span data-ttu-id="07100-145">Környezetek létrehozásához be kell jelentkeznie az Azure-ba.</span><span class="sxs-lookup"><span data-stu-id="07100-145">To create a context, you must be logged in to Azure.</span></span> <span data-ttu-id="07100-146">Az `Add-AzureRmAccount` parancsmaggal (vagy az aliasával, a `Login-AzureRmAccount` parancsmaggal) állítható be a későbbiekben futtatott Azure PowerShell-parancsmagok által használt alapértelmezett környezet, valamint lehetővé teszi a bejelentkezési hitelesítő adatai számára engedélyezett bérlők vagy előfizetések elérését.</span><span class="sxs-lookup"><span data-stu-id="07100-146">The `Add-AzureRmAccount` cmdlet (or its alias, `Login-AzureRmAccount`) sets the default context used by subsequent Azure PowerShell cmdlets, and allows you to access any tenants or subscriptions allowed by your login credentials.</span></span>

<span data-ttu-id="07100-147">A bejelentkezés után új környezet hozzáadásához használja a `Set-AzureRmContext` parancsmagot (vagy az aliasát, a `Select-AzureRmSubscription` parancsmagot).</span><span class="sxs-lookup"><span data-stu-id="07100-147">To add a new context after login, use `Set-AzureRmContext` (or its alias, `Select-AzureRmSubscription`).</span></span>

```powershell
PS C:\> Set-AzureRMContext -Subscription "Contoso Subscription 1" -Name "Contoso1"
```

<span data-ttu-id="07100-148">Az előző példa hozzáad egy új környezetet, amely a „Contoso Subscription 1” nevű előfizetést célozza az aktuális hitelesítő adatokkal.</span><span class="sxs-lookup"><span data-stu-id="07100-148">The previous example adds a new context targeting 'Contoso Subscription 1' using your current credentials.</span></span> <span data-ttu-id="07100-149">Az új környezet neve „Contoso1”.</span><span class="sxs-lookup"><span data-stu-id="07100-149">The new context is named 'Contoso1'.</span></span> <span data-ttu-id="07100-150">Ha nem ad meg nevet a környezetnek, a rendszer egy alapértelmezett nevet ad a használt fiók- és előfizetés-azonosító alapján.</span><span class="sxs-lookup"><span data-stu-id="07100-150">If you do not provide a name for the context, a default name, using the account ID and subscription ID is used.</span></span>

<span data-ttu-id="07100-151">Meglévő környezetek átnevezéséhez használja a `Rename-AzureRmContext` parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="07100-151">To rename an existing context, use the `Rename-AzureRmContext` cmdlet.</span></span> <span data-ttu-id="07100-152">Például:</span><span class="sxs-lookup"><span data-stu-id="07100-152">For example:</span></span>

```powershell
PS C:\> Rename-AzureRmContext '[user1@contoso.org; 123456-7890-1234-564321]` 'Contoso2'
```

<span data-ttu-id="07100-153">A példa az automatikusan elnevezett `[user1@contoso.org; 123456-7890-1234-564321]` környezetet átnevezi az egyszerű „Contoso2” névre.</span><span class="sxs-lookup"><span data-stu-id="07100-153">This example renames the context with automatic name `[user1@contoso.org; 123456-7890-1234-564321]` to the simple name 'Contoso2'.</span></span> <span data-ttu-id="07100-154">A környezetek kezelésére szolgáló parancsmagok parancssori kiegészítés funkcióval rendelkeznek, így a beírásukkor gyorsan kiválasztható a környezet.</span><span class="sxs-lookup"><span data-stu-id="07100-154">Cmdlets that manage contexts also use tab completion, allowing you to quickly select the context.</span></span>

<span data-ttu-id="07100-155">A környezet a `Remove-AzureRmContext` parancsmaggal távolítható el.</span><span class="sxs-lookup"><span data-stu-id="07100-155">Finally, to remove a context, use the `Remove-AzureRmContext` cmdlet.</span></span>  <span data-ttu-id="07100-156">Például:</span><span class="sxs-lookup"><span data-stu-id="07100-156">For example:</span></span>

```powershell
PS C:\> Remove-AzureRmContext Contoso2
```

<span data-ttu-id="07100-157">Elfelejti a „Contoso2” nevű környezetet.</span><span class="sxs-lookup"><span data-stu-id="07100-157">Forgets the context that was named 'Contoso2'.</span></span> <span data-ttu-id="07100-158">A környezet ezután a `Set-AzureRmContext` parancsmaggal hozható újra létre</span><span class="sxs-lookup"><span data-stu-id="07100-158">You can recreate this context subsequently using `Set-AzureRmContext`</span></span>

## <a name="removing-credentials"></a><span data-ttu-id="07100-159">Hitelesítő adatok eltávolítása</span><span class="sxs-lookup"><span data-stu-id="07100-159">Removing credentials</span></span>

<span data-ttu-id="07100-160">Egy adott felhasználó vagy szolgáltatásnév összes hitelesítő adatát és társított környezetét a `Remove-AzureRmAccount` (vagy más néven `Logout-AzureRmAccount`) parancsmaggal távolíthatja el.</span><span class="sxs-lookup"><span data-stu-id="07100-160">You can remove all credentials and associated contexts for a user or service principal using `Remove-AzureRmAccount` (also known as `Logout-AzureRmAccount`).</span></span> <span data-ttu-id="07100-161">Paraméterek nélkül a `Remove-AzureRmAccount` parancsmag az aktuális környezetben bejelentkezett felhasználó vagy szolgáltatásnév összes társított hitelesítő adatát és környezetét eltávolítja.</span><span class="sxs-lookup"><span data-stu-id="07100-161">When executed without parameters, the `Remove-AzureRmAccount` cmdlet removes all credentials and contexts associated with the User or Service Principal in the current context.</span></span> <span data-ttu-id="07100-162">A parancsmagnak átadható egy felhasználónév, egyszerű szolgáltatásnév vagy egy környezet is, ha egy adott szolgáltatást kíván megcélozni.</span><span class="sxs-lookup"><span data-stu-id="07100-162">You may pass in a Username, Service Principal Name, or context to target a particular principal.</span></span>

```powershell
Remove-AzureRmAccount user1@contoso.org
```

## <a name="using-context-scopes"></a><span data-ttu-id="07100-163">Környezeti hatókörök használata</span><span class="sxs-lookup"><span data-stu-id="07100-163">Using context scopes</span></span>

<span data-ttu-id="07100-164">Előfordulhat, hogy úgy szeretné kiválasztani, módosítani vagy eltávolítani egy PowerShell-munkamenet valamely környezetét, hogy a többi munkamenetet ne érintse a módosítás.</span><span class="sxs-lookup"><span data-stu-id="07100-164">Occasionally, you may want to select, change, or remove a context in a PowerShell session without impacting other sessions.</span></span> <span data-ttu-id="07100-165">A környezeti parancsmagok alapértelmezett viselkedésének módosításához használja a `Scope` paramétert.</span><span class="sxs-lookup"><span data-stu-id="07100-165">To change the default behavior of context cmdlets, use the `Scope` parameter.</span></span> <span data-ttu-id="07100-166">A `Process` hatókör felülírja az alapértelmezett viselkedést, hogy csak az aktuális munkamenetre vonatkozzon.</span><span class="sxs-lookup"><span data-stu-id="07100-166">The `Process` scope overrides the default behavior by making it apply only for the current session.</span></span> <span data-ttu-id="07100-167">A `CurrentUser` hatókör ezzel szemben nemcsak az aktuális, hanem minden munkamenetben módosítja a környezetet.</span><span class="sxs-lookup"><span data-stu-id="07100-167">Conversely `CurrentUser` scope changes the context in all sessions, instead of just the current session.</span></span>

<span data-ttu-id="07100-168">Ha például anélkül szeretné módosítani az aktuális PowerShell-munkamenet alapértelmezett környezetét, hogy a módosítás a többi ablakot vagy a munkamenet következő megnyitásakor használt környezetet is érintené, használja a következő parancsmagot:</span><span class="sxs-lookup"><span data-stu-id="07100-168">As an example, to change the default context in the current PowerShell session without impacting other windows, or the context used the next time a session is opened, use:</span></span>

```powershell
PS C:\> Select-AzureRmContext Contoso1 -Scope Process
```

## <a name="how-the-context-autosave-setting-is-remembered"></a><span data-ttu-id="07100-169">A környezet automatikus mentési beállításainak megőrzése</span><span class="sxs-lookup"><span data-stu-id="07100-169">How the context autosave setting is remembered</span></span>

<span data-ttu-id="07100-170">A rendszer a felhasználó Azure PowerShell-könyvtárába (`%AppData%\Roaming\Windows Azure PowerShell`) menti a környezet automatikus mentési beállításait.</span><span class="sxs-lookup"><span data-stu-id="07100-170">The context AutoSave setting is saved to the user Azure PowerShell directory (`%AppData%\Roaming\Windows Azure PowerShell`).</span></span> <span data-ttu-id="07100-171">Előfordulhat, hogy egyes számítógépfiókok nem rendelkeznek hozzáféréshez ehhez a könyvtárhoz.</span><span class="sxs-lookup"><span data-stu-id="07100-171">Some kinds of computer accounts may not have access to this directory.</span></span> <span data-ttu-id="07100-172">Ilyen esetekben használhatja a következő környezeti változót:</span><span class="sxs-lookup"><span data-stu-id="07100-172">For such scenarios, you can use the environment variable</span></span>

```powershell
$env:AzureRmContextAutoSave="true" | "false"
```

<span data-ttu-id="07100-173">Ha a változó értéke „true”, a rendszer automatikusan menti a környezetet.</span><span class="sxs-lookup"><span data-stu-id="07100-173">If set to 'true', the context is automatically saved.</span></span> <span data-ttu-id="07100-174">Ha az érték „false”, a rendszer nem menti a környezetet.</span><span class="sxs-lookup"><span data-stu-id="07100-174">If set to 'false', the context is not saved.</span></span>

## <a name="changes-to-the-azurermprofile-module"></a><span data-ttu-id="07100-175">Az AzureRM.Profile modul változásai</span><span class="sxs-lookup"><span data-stu-id="07100-175">Changes to the AzureRM.Profile module</span></span>

<span data-ttu-id="07100-176">Új parancsmagok a környezetek kezeléséhez</span><span class="sxs-lookup"><span data-stu-id="07100-176">New cmdlets for managing context</span></span>

- <span data-ttu-id="07100-177">[Enable-AzureRmContextAutosave][enable] – A környezet mentésének engedélyezése a PowerShell-munkamenetek között.</span><span class="sxs-lookup"><span data-stu-id="07100-177">[Enable-AzureRmContextAutosave][enable] - Allow saving the context between powershell sessions.</span></span>
  <span data-ttu-id="07100-178">Minden változás módosítja a globális környezetet.</span><span class="sxs-lookup"><span data-stu-id="07100-178">Any changes alter the global context.</span></span>
- <span data-ttu-id="07100-179">[Disable-AzureRmContextAutosave][disable] – A környezet automatikus mentésének letiltása.</span><span class="sxs-lookup"><span data-stu-id="07100-179">[Disable-AzureRmContextAutosave][disable] - Turn off autosaving the context.</span></span> <span data-ttu-id="07100-180">Minden egyes új PowerShell-munkamenetnek újra be kell jelentkeznie.</span><span class="sxs-lookup"><span data-stu-id="07100-180">Each new PowerShell session is required to log in again.</span></span>
- <span data-ttu-id="07100-181">[Select-AzureRmContext][select] – Az alapértelmezett környezet kiválasztása.</span><span class="sxs-lookup"><span data-stu-id="07100-181">[Select-AzureRmContext][select] - Select a context as the default.</span></span> <span data-ttu-id="07100-182">Az ezt követő parancsmagok ennek a környezetnek a hitelesítő adatait használják.</span><span class="sxs-lookup"><span data-stu-id="07100-182">All subsequent cmdlets use the credentials in this context for authentication.</span></span>
- <span data-ttu-id="07100-183">[Remove-AzureRmAccount][remove-cred] – Adott fiókkal társított összes hitelesítő adat és környezet eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="07100-183">[Remove-AzureRmAccount][remove-cred] - Remove all credentials and contexts associated with an account.</span></span>
- <span data-ttu-id="07100-184">[Remove-AzureRmContext][remove-context] – A megnevezett környezet eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="07100-184">[Remove-AzureRmContext][remove-context] - Remove a named context.</span></span>
- <span data-ttu-id="07100-185">[Rename-AzureRmContext][rename] – Meglévő környezet eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="07100-185">[Rename-AzureRmContext][rename] - Rename an existing context.</span></span>

<span data-ttu-id="07100-186">Meglévő profilparancsmagok változásai</span><span class="sxs-lookup"><span data-stu-id="07100-186">Changes to existing profile cmdlets</span></span>

- <span data-ttu-id="07100-187">[Add-AzureRmAccount][login] – Lehetővé teszi a bejelentkezés hatókörének beállítását a folyamatra vagy az aktuális felhasználóra.</span><span class="sxs-lookup"><span data-stu-id="07100-187">[Add-AzureRmAccount][login] - Allow scoping of the login to the process or the current user.</span></span>
  <span data-ttu-id="07100-188">Lehetővé teszi az alapértelmezett környezet elnevezését a bejelentkezés után.</span><span class="sxs-lookup"><span data-stu-id="07100-188">Allow naming the default context after login.</span></span>
- <span data-ttu-id="07100-189">[Import-AzureRmContext][import] – Lehetővé teszi a bejelentkezés hatókörének beállítását a folyamatra vagy az aktuális felhasználóra.</span><span class="sxs-lookup"><span data-stu-id="07100-189">[Import-AzureRmContext][import] - Allow scoping of the login to the process or the current user.</span></span>
- <span data-ttu-id="07100-190">[Set-AzureRmContext][set-context] – Lehetővé teszi meglévő megnevezett környezetek kiválasztását, valamint a hatókör beállítását a folyamatra vagy az aktuális felhasználóra.</span><span class="sxs-lookup"><span data-stu-id="07100-190">[Set-AzureRmContext][set-context] - Allow selection of existing named contexts, and scope changes to the process or current user.</span></span>

<!-- Hyperlinks -->
[enable]: /powershell/module/azurerm.profile/Enable-AzureRmContextAutosave
[disable]: /powershell/module/azurerm.profile/Disable-AzureRmContextAutosave
[select]: /powershell/module/azurerm.profile/Select-AzureRmContext
[remove-cred]: /powershell/module/azurerm.profile/Remove-AzureRmAccount
[remove-context]: /powershell/module/azurerm.profile/Remove-AzureRmContext
[rename]: /powershell/module/azurerm.profile/Rename-AzureRmContext

<!-- Updated cmdlets -->
[login]: /powershell/module/azurerm.profile/Add-AzureRmAccount
[import]: /powershell/module/azurerm.profile/Import-AzureRmAccount
[set-context]: /powershell/module/azurerm.profile/Import-AzureRmContext
