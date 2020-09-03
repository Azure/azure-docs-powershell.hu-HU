---
title: Azure-környezetek és bejelentkezési hitelesítő adatok
description: A cikkből megismerheti, hogyan használhatók fel újra az Azure-beli hitelesítő és egyéb adatok több PowerShell-munkamenet során.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 10/21/2019
ms.custom: devx-track-azurepowershell
ms.openlocfilehash: b6ac8b821f2d88431be67fd5fe1d50fc640d2b8f
ms.sourcegitcommit: 8b3126b5c79f453464d90669f0046ba86b7a3424
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 09/01/2020
ms.locfileid: "89242001"
---
# <a name="azure-powershell-context-objects"></a><span data-ttu-id="2eba8-103">Azure PowerShell környezeti objektumok</span><span class="sxs-lookup"><span data-stu-id="2eba8-103">Azure PowerShell context objects</span></span>

<span data-ttu-id="2eba8-104">Az Azure PowerShell _Azure PowerShell környezeti objektumokat_ (Azure-környezeteket) használ az előfizetési és a hitelesítési információk tárolására.</span><span class="sxs-lookup"><span data-stu-id="2eba8-104">Azure PowerShell uses _Azure PowerShell context objects_ (Azure contexts) to hold subscription and authentication information.</span></span> <span data-ttu-id="2eba8-105">Ha több előfizetéssel is rendelkezik, az Azure-környezetekben kiválaszthatja azt az előfizetést, amelyben futtatni szeretné az Azure PowerShell-parancsmagokat.</span><span class="sxs-lookup"><span data-stu-id="2eba8-105">If you have more than one subscription, Azure contexts let you select the subscription to run Azure PowerShell cmdlets on.</span></span> <span data-ttu-id="2eba8-106">Az Azure-környezetek a bejelentkezési adatok több PowerShell-munkamenetre kiterjedő tárolására, illetve a háttérfeladatok futtatására is használhatók.</span><span class="sxs-lookup"><span data-stu-id="2eba8-106">Azure contexts are also used to store sign-in information across multiple PowerShell sessions and run background tasks.</span></span>

<span data-ttu-id="2eba8-107">Ez a cikk az Azure-környezetek kezelését ismerteti, az előfizetések és a fiókok kezelésére nem tér ki.</span><span class="sxs-lookup"><span data-stu-id="2eba8-107">This article covers managing Azure contexts, not the management of subscriptions or accounts.</span></span> <span data-ttu-id="2eba8-108">Ha felhasználók, előfizetések, bérlők vagy más fiókadatok kezelése iránt érdeklődik, tekintse át az [Azure Active Directory](/azure/active-directory) dokumentációját.</span><span class="sxs-lookup"><span data-stu-id="2eba8-108">If you're looking to manage users, subscriptions, tenants, or other account information, see the [Azure Active Directory](/azure/active-directory) documentation.</span></span> <span data-ttu-id="2eba8-109">A környezetek háttér- vagy párhuzamos feladatok futtatására való használatával kapcsolatban tekintse meg [az Azure PowerShell-parancsmagok PowerShell-feladatokban való használatát](using-psjobs.md) ismertető cikket, miután megismerkedett az Azure-környezetekkel.</span><span class="sxs-lookup"><span data-stu-id="2eba8-109">To learn about using contexts for running background or parallel tasks, see [Use Azure PowerShell cmdlets in PowerShell jobs](using-psjobs.md) after becoming familiar with Azure contexts.</span></span>

## <a name="overview-of-azure-context-objects"></a><span data-ttu-id="2eba8-110">Az Azure-beli környezeti objektumok áttekintése</span><span class="sxs-lookup"><span data-stu-id="2eba8-110">Overview of Azure context objects</span></span>

<span data-ttu-id="2eba8-111">Az Azure-környezetek olyan PowerShell-objektumok, amelyek a parancsok futtatásához kiválasztott aktív előfizetést, illetve az Azure-felhőkhöz való csatlakozáshoz szükséges hitelesítő adatokat képviselik.</span><span class="sxs-lookup"><span data-stu-id="2eba8-111">Azure contexts are PowerShell objects representing your active subscription to run commands against, and the authentication information needed to connect to an Azure cloud.</span></span> <span data-ttu-id="2eba8-112">Az Azure-környezeteknek köszönhetően az Azure PowerShellnek nem kell az előfizetések közötti váltáskor újból és újból hitelesítenie a fiókját.</span><span class="sxs-lookup"><span data-stu-id="2eba8-112">With Azure contexts, Azure PowerShell doesn't need to reauthenticate your account each time you switch subscriptions.</span></span> <span data-ttu-id="2eba8-113">Az Azure-környezetek a következőkből állnak:</span><span class="sxs-lookup"><span data-stu-id="2eba8-113">An Azure context consists of:</span></span>

* <span data-ttu-id="2eba8-114">A _fiókból_, amelyet az Azure-ba való bejelentkezéshez használt a [Connect-AzAccount](/powershell/module/az.accounts/connect-azaccount) parancsmaggal.</span><span class="sxs-lookup"><span data-stu-id="2eba8-114">The _account_ that was used to sign in to Azure with [Connect-AzAccount](/powershell/module/az.accounts/connect-azaccount).</span></span> <span data-ttu-id="2eba8-115">Az Azure-környezetek a fiókok szempontjából ugyanúgy kezelik a felhasználókat, az alkalmazásazonosítókat és a szolgáltatásneveket.</span><span class="sxs-lookup"><span data-stu-id="2eba8-115">Azure contexts treat users, application IDs, and service principals the same from an account perspective.</span></span>
* <span data-ttu-id="2eba8-116">Az aktív _előfizetésből_, azaz egy adott _bérlőhöz_ társított Azure-erőforrások létrehozására és futtatására vonatkozó, Microsofttal kötött szolgáltatási szerződésből.</span><span class="sxs-lookup"><span data-stu-id="2eba8-116">The active _subscription_, a service agreement with Microsoft to create and run Azure resources, which are associated with a _tenant_.</span></span> <span data-ttu-id="2eba8-117">A bérlőket gyakran _szervezeteknek_ is nevezik a dokumentációkban vagy az Active Directory használata során.</span><span class="sxs-lookup"><span data-stu-id="2eba8-117">Tenants are often referred to as _organizations_ in documentation or when working with Active Directory.</span></span>
* <span data-ttu-id="2eba8-118">Egy _jogkivonat-gyorsítótárra_, azaz egy, az Azure-felhők elérésére használt, tárolt hitelesítési jogkivonatra mutató hivatkozásból.</span><span class="sxs-lookup"><span data-stu-id="2eba8-118">A reference to a _token cache_, a stored authentication token for accessing an Azure cloud.</span></span> <span data-ttu-id="2eba8-119">A [környezet automatikus mentésére vonatkozó beállítások](#save-azure-contexts-across-powershell-sessions) határozzák meg, hogy a rendszer hol tárolja és mennyi ideig őrzi meg a jogkivonatot.</span><span class="sxs-lookup"><span data-stu-id="2eba8-119">Where this token is stored and how long it persists for is determined by the [context autosave settings](#save-azure-contexts-across-powershell-sessions).</span></span>

<span data-ttu-id="2eba8-120">A kifejezésekkel kapcsolatos további információkért lásd [az Azure Active Directory terminológiáját](/azure/active-directory/fundamentals/active-directory-whatis#terminology).</span><span class="sxs-lookup"><span data-stu-id="2eba8-120">For more information on these terms, see [Azure Active Directory Terminology](/azure/active-directory/fundamentals/active-directory-whatis#terminology).</span></span> <span data-ttu-id="2eba8-121">Az Azure-környezetek által használt hitelesítési jogkivonatok ugyanolyanok, mint az állandó munkamenet részét képező többi tárolt jogkivonat.</span><span class="sxs-lookup"><span data-stu-id="2eba8-121">Authentication tokens used by Azure contexts are the same as other stored tokens that are part of a persistent session.</span></span> 

<span data-ttu-id="2eba8-122">Amikor bejelentkezik a `Connect-AzAccount` parancsmaggal, a rendszer legalább egy Azure-környezetet létrehoz az alapértelmezett előfizetéshez.</span><span class="sxs-lookup"><span data-stu-id="2eba8-122">When you sign in with `Connect-AzAccount`, at least one Azure context is created for your default subscription.</span></span> <span data-ttu-id="2eba8-123">A `Connect-AzAccount` által visszaadott objektum a PowerShell-munkamenet hátralévő részéhez használt alapértelmezett Azure-környezet.</span><span class="sxs-lookup"><span data-stu-id="2eba8-123">The object returned by `Connect-AzAccount` is the default Azure context used for the rest of the PowerShell session.</span></span>

## <a name="get-azure-contexts"></a><span data-ttu-id="2eba8-124">Azure-környezetek lekérése</span><span class="sxs-lookup"><span data-stu-id="2eba8-124">Get Azure contexts</span></span>

<span data-ttu-id="2eba8-125">Az elérhető Azure-környezeteket a [Get-AzContext](/powershell/module/az.accounts/get-azcontext) parancsmaggal lehet lekérni.</span><span class="sxs-lookup"><span data-stu-id="2eba8-125">Available Azure contexts are retrieved with the [Get-AzContext](/powershell/module/az.accounts/get-azcontext) cmdlet.</span></span> <span data-ttu-id="2eba8-126">Az összes elérhető környezetet a `-ListAvailable` argumentummal lehet megjeleníteni:</span><span class="sxs-lookup"><span data-stu-id="2eba8-126">List all of the available contexts with `-ListAvailable`:</span></span>

```azurepowershell-interactive
Get-AzContext -ListAvailable
```

<span data-ttu-id="2eba8-127">Azt is megteheti, hogy név alapján kér le egy környezetet:</span><span class="sxs-lookup"><span data-stu-id="2eba8-127">Or get a context by name:</span></span>

```azurepowershell-interactive
$context = Get-AzContext -Name "mycontext"
```

<span data-ttu-id="2eba8-128">A környezetek nevei eltérhetnek a társított előfizetés nevétől.</span><span class="sxs-lookup"><span data-stu-id="2eba8-128">Context names may be different from the name of the associated subscription.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="2eba8-129">Az elérhető Azure-környezetek __nem__ mindig azonosak az elérhető előfizetésekkel.</span><span class="sxs-lookup"><span data-stu-id="2eba8-129">The available Azure contexts __aren't__ always your available subscriptions.</span></span> <span data-ttu-id="2eba8-130">Az Azure-környezetek csak a helyben tárolt adatokat jelölik.</span><span class="sxs-lookup"><span data-stu-id="2eba8-130">Azure contexts only represent locally-stored information.</span></span> <span data-ttu-id="2eba8-131">Az előfizetéseit a [Get-AzSubscription](/powershell/module/Az.Accounts/Get-AzSubscription?view=azps-1.8.0) parancsmaggal kérheti le.</span><span class="sxs-lookup"><span data-stu-id="2eba8-131">You can get your subscriptions with the [Get-AzSubscription](/powershell/module/Az.Accounts/Get-AzSubscription?view=azps-1.8.0) cmdlet.</span></span>

## <a name="create-a-new-azure-context-from-subscription-information"></a><span data-ttu-id="2eba8-132">Új Azure-környezet létrehozása előfizetési adatokból</span><span class="sxs-lookup"><span data-stu-id="2eba8-132">Create a new Azure context from subscription information</span></span>

<span data-ttu-id="2eba8-133">A [Set-AzContext](/powershell/module/Az.Accounts/Set-AzContext) parancsmaggal új Azure-környezeteket hozhat létre, és be is állíthatja őket aktív környezetként.</span><span class="sxs-lookup"><span data-stu-id="2eba8-133">The [Set-AzContext](/powershell/module/Az.Accounts/Set-AzContext) cmdlet is used to both create new Azure contexts and set them as the active context.</span></span>
<span data-ttu-id="2eba8-134">Az új Azure-környezetek létrehozásának legegyszerűbb módja a meglévő előfizetési adatok használata.</span><span class="sxs-lookup"><span data-stu-id="2eba8-134">The easiest way to create a new Azure context is to use existing subscription information.</span></span> <span data-ttu-id="2eba8-135">A parancsmagot arra tervezték, hogy átirányított értékként kivegye a `Get-AzSubscription` kimeneti objektumát, és konfiguráljon egy új Azure-környezetet:</span><span class="sxs-lookup"><span data-stu-id="2eba8-135">The cmdlet is designed to take the output object from `Get-AzSubscription` as a piped value and configure a new Azure context:</span></span>

```azurepowershell-interactive
Get-AzSubscription -SubscriptionName 'MySubscriptionName' | Set-AzContext -Name 'MyContextName'
```

<span data-ttu-id="2eba8-136">Azt is megteheti, hogy megadja az előfizetés nevét vagy azonosítóját, és szükség esetén a bérlőazonosítót:</span><span class="sxs-lookup"><span data-stu-id="2eba8-136">Or give the subscription name or ID and the tenant ID if necessary:</span></span>

```azurepowershell-interactive
Set-AzContext -Name 'MyContextName' -Subscription 'MySubscriptionName' -Tenant '.......'
```

<span data-ttu-id="2eba8-137">Ha a `-Name` argumentum kimarad, a rendszer az előfizetés nevét és azonosítóját használja a környezet neveként, `Subscription Name (subscription-id)` formátumban.</span><span class="sxs-lookup"><span data-stu-id="2eba8-137">If the `-Name` argument is omitted, then the subscription's name and ID are used as the context name in the format `Subscription Name (subscription-id)`.</span></span>

## <a name="change-the-active-azure-context"></a><span data-ttu-id="2eba8-138">Az aktív Azure-környezet módosítása</span><span class="sxs-lookup"><span data-stu-id="2eba8-138">Change the active Azure context</span></span>

<span data-ttu-id="2eba8-139">Az aktív Azure-környezetet a `Set-AzContext` és a [Select-AzContext](/powershell/module/az.accounts/set-azcontext) parancsmaggal is meg lehet változtatni.</span><span class="sxs-lookup"><span data-stu-id="2eba8-139">Both `Set-AzContext` and [Select-AzContext](/powershell/module/az.accounts/set-azcontext) can be used to change the active Azure context.</span></span> <span data-ttu-id="2eba8-140">Az [új Azure-környezet létrehozásával](#create-a-new-azure-context-from-subscription-information) foglalkozó szakaszban leírtak szerint a `Set-AzContext` létrehoz egy új Azure-környezetet egy előfizetéshez, ha annak még nincs környezete, majd beállítja aktívként.</span><span class="sxs-lookup"><span data-stu-id="2eba8-140">As described in [Create a new Azure context](#create-a-new-azure-context-from-subscription-information), `Set-AzContext` creates a new Azure context for a subscription if one doesn't exist, and then switches to use that context as the active one.</span></span>

<span data-ttu-id="2eba8-141">A `Select-AzContext` csak a meglévő Azure-környezetekkel használható. Hasonlóan működik, mint a `Set-AzContext -Context`, de átadáshoz tervezték:</span><span class="sxs-lookup"><span data-stu-id="2eba8-141">`Select-AzContext` is meant to be used with existing Azure contexts only and works similarly to using `Set-AzContext -Context`, but is designed for use with piping:</span></span>

```azurepowershell-interactive
Set-AzContext -Context $(Get-AzContext -Name "mycontext") # Set a context with an inline Azure context object
Get-AzContext -Name "mycontext" | Select-AzContext # Set a context with a piped Azure context object
```

<span data-ttu-id="2eba8-142">Az Azure PowerShell számos más fiók- és környezetkezelési parancsához hasonlóan a `Set-AzContext` és a `Select-AzContext` támogatja a `-Scope` argumentumot, így Ön szabályozhatja, hogy mennyi ideig legyen aktív a környezet.</span><span class="sxs-lookup"><span data-stu-id="2eba8-142">Like many other account and context management commands in Azure PowerShell, `Set-AzContext` and `Select-AzContext` support the `-Scope` argument so that you can control how long the context is active.</span></span> <span data-ttu-id="2eba8-143">A `-Scope` argumentummal meg lehet változtatni egyetlen munkamenet aktív környezetét, az alapértelmezett érték módosítása nélkül:</span><span class="sxs-lookup"><span data-stu-id="2eba8-143">`-Scope` lets you change a single session's active context without changing the default:</span></span>

```azurepowershell-interactive
Get-AzContext -Name "mycontext" | Select-AzContext -Scope Process
```

<span data-ttu-id="2eba8-144">Ha el szeretné kerülni, hogy a rendszer a teljes PowerShell-munkamenetre vonatkozóan lecserélje a környezetet, az Azure PowerShell-parancsokat egy adott környezetben is futtathatja az `-AzContext` argumentummal:</span><span class="sxs-lookup"><span data-stu-id="2eba8-144">To avoid switching contexts for a whole PowerShell session, all Azure PowerShell commands can be run against a given context with the `-AzContext` argument:</span></span>

```azurepowershell-interactive
$context = Get-AzContext -Name "mycontext"
New-AzVM -Name ExampleVM -AzContext $context
```

<span data-ttu-id="2eba8-145">A környezetek Azure PowerShell-parancsmagokkal való használatának másik fő felhasználási módja a parancsok háttérbeli futtatása.</span><span class="sxs-lookup"><span data-stu-id="2eba8-145">The other main use of contexts with Azure PowerShell cmdlets is to run background commands.</span></span> <span data-ttu-id="2eba8-146">A PowerShell-feladatok Azure PowerShell-lel történő futtatásával kapcsolatos további információkért lásd: [Azure PowerShell-parancsmagok futtatása PowerShell-feladatokban](using-psjobs.md).</span><span class="sxs-lookup"><span data-stu-id="2eba8-146">To learn more about running PowerShell Jobs using Azure PowerShell, see [Run Azure PowerShell cmdlets in PowerShell Jobs](using-psjobs.md).</span></span>

## <a name="save-azure-contexts-across-powershell-sessions"></a><span data-ttu-id="2eba8-147">Azure-környezetek több PowerShell-munkamenetre kiterjedő mentése</span><span class="sxs-lookup"><span data-stu-id="2eba8-147">Save Azure contexts across PowerShell sessions</span></span>

<span data-ttu-id="2eba8-148">A rendszer alapértelmezés szerint menti az Azure-környezeteket, hogy több PowerShell-munkamenetben is használhatók legyenek.</span><span class="sxs-lookup"><span data-stu-id="2eba8-148">By default, Azure contexts are saved for use between PowerShell sessions.</span></span> <span data-ttu-id="2eba8-149">Az alábbiak szerint módosíthatja ezt a viselkedést:</span><span class="sxs-lookup"><span data-stu-id="2eba8-149">You change this behavior in the following ways:</span></span>

* <span data-ttu-id="2eba8-150">Jelentkezzen be a `-Scope Process` és a `Connect-AzAccount` használatával.</span><span class="sxs-lookup"><span data-stu-id="2eba8-150">Sign in using `-Scope Process` with `Connect-AzAccount`.</span></span>

  ```azurepowershell
  Connect-AzAccount -Scope Process
  ```

  <span data-ttu-id="2eba8-151">A bejelentkezés részeként visszaadott Azure-környezet _csak_ az aktuális munkamenetre érvényes, és a rendszer az Azure PowerShell-környezet automatikus mentési beállításától függetlenül nem fogja automatikusan menteni.</span><span class="sxs-lookup"><span data-stu-id="2eba8-151">The Azure context returned as part of this sign in is valid for the current session _only_ and will not be automatically saved, regardless of the Azure PowerShell context autosave setting.</span></span>
* <span data-ttu-id="2eba8-152">Tiltsa le az Azure PowerShell környezeteinek automatikus mentését a [Disable-AzContextAutosave](/powershell/module/az.accounts/disable-azcontextautosave) parancsmaggal.</span><span class="sxs-lookup"><span data-stu-id="2eba8-152">Disable AzurePowershell's context autosave with the [Disable-AzContextAutosave](/powershell/module/az.accounts/disable-azcontextautosave) cmdlet.</span></span>
  <span data-ttu-id="2eba8-153">A környezet automatikus mentésének letiltása __nem__ törli a tárolt jogkivonatokat.</span><span class="sxs-lookup"><span data-stu-id="2eba8-153">Disabling context autosave __doesn't__ clear any stored tokens.</span></span> <span data-ttu-id="2eba8-154">A tárolt Azure-beli környezeti adatok törlésével kapcsolatban lásd az [Azure-környezetek és hitelesítő adatok eltávolításával](#remove-azure-contexts-and-stored-credentials) foglalkozó szakaszt.</span><span class="sxs-lookup"><span data-stu-id="2eba8-154">To learn how to clear stored Azure context information, see [Remove Azure contexts and credentials](#remove-azure-contexts-and-stored-credentials).</span></span>
* <span data-ttu-id="2eba8-155">Explicit módon engedélyezze az Azure-környezet automatikus mentését. Ezt az [Enable-AzContextAutosave](/powershell/module/az.accounts/enable-azcontextautosave) parancsmaggal teheti meg.</span><span class="sxs-lookup"><span data-stu-id="2eba8-155">Explicitly enable Azure context autosave can be enabled with the [Enable-AzContextAutosave](/powershell/module/az.accounts/enable-azcontextautosave) cmdlet.</span></span> <span data-ttu-id="2eba8-156">Ha engedélyezte az automatikus mentést, a rendszer helyben fogja tárolni a felhasználó környezeteit a későbbi PowerShell-munkamenetek számára.</span><span class="sxs-lookup"><span data-stu-id="2eba8-156">With autosave enabled, all of a user's contexts are stored locally for later PowerShell sessions.</span></span>
* <span data-ttu-id="2eba8-157">Mentse manuálisan a környezeteket a [Save-AzContext](/powershell/module/az.accounts/save-azcontext) parancsmaggal a későbbi PowerShell-munkamenetekben való használathoz, amelyekbe az [Import-AzContext](/powershell/module/az.accounts/import-azcontext) parancsmaggal tölthetők be:</span><span class="sxs-lookup"><span data-stu-id="2eba8-157">Manually save contexts with [Save-AzContext](/powershell/module/az.accounts/save-azcontext) to be used in future PowerShell sessions, where they can be loaded with [Import-AzContext](/powershell/module/az.accounts/import-azcontext):</span></span>

  ```azurepowershell
  Save-AzContext -Path current-context.json # Save the current context
  Save-AzContext -Profile $profileObject -Path other-context.json # Save a context object
  Import-AzContext -Path other-context.json # Load the context from a file and set it to the current context
  ```

> [!WARNING]
> <span data-ttu-id="2eba8-158">A környezet automatikus mentésének letiltása __nem__ törli a mentett környezeti adatokat.</span><span class="sxs-lookup"><span data-stu-id="2eba8-158">Disabling context autosave __doesn't__ clear any stored context information that was saved.</span></span> <span data-ttu-id="2eba8-159">A tárolt adatok eltávolításához használja a [Clear-AzContext](/powershell/module/az.accounts/Clear-AzContext) parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="2eba8-159">To remove stored information, use the [Clear-AzContext](/powershell/module/az.accounts/Clear-AzContext) cmdlet.</span></span> <span data-ttu-id="2eba8-160">A mentett környezetek eltávolításával kapcsolatos további információkért lásd a [környezetek és hitelesítő adatok eltávolításával](#remove-azure-contexts-and-stored-credentials) foglalkozó szakaszt.</span><span class="sxs-lookup"><span data-stu-id="2eba8-160">For more on removing saved contexts, see [Remove contexts and credentials](#remove-azure-contexts-and-stored-credentials).</span></span>

<span data-ttu-id="2eba8-161">Mindegyik parancs támogatja a `-Scope` paramétert, ami fel tudja venni a `Process` értéket, hogy csak a jelenleg futó folyamatra vonatkozzon.</span><span class="sxs-lookup"><span data-stu-id="2eba8-161">Each of these commands supports the `-Scope` parameter, which can take a value of `Process` to only apply to the current running process.</span></span> <span data-ttu-id="2eba8-162">Adja meg például a következőt, ha gondoskodni szeretne róla, hogy a rendszer ne mentse az újonnan létrehozott környezeteket a PowerShell-munkamenetből való kilépés után:</span><span class="sxs-lookup"><span data-stu-id="2eba8-162">For example, to ensure that newly created contexts aren't saved after exiting a PowerShell session:</span></span>

```azurepowershell-interactive
Disable-AzContextAutosave -Scope Process
$context2 = Set-AzContext -Subscription "sub-id" -Tenant "other-tenant"
```

<span data-ttu-id="2eba8-163">A Windows az `$env:USERPROFILE\.Azure` könyvtárban tárolja a környezetek adatait és a jogkivonatokat, más platformok pedig a `$HOME/.Azure` könyvtárban.</span><span class="sxs-lookup"><span data-stu-id="2eba8-163">Context information and tokens are stored in the `$env:USERPROFILE\.Azure` directory on Windows, and on `$HOME/.Azure` on other platforms.</span></span> <span data-ttu-id="2eba8-164">Előfordulhat, hogy a tárolt adatok között megtalálható bizalmas adatokat, például az előfizetési azonosítókat és bérlőazonosítókat továbbra is el lehet érni a naplókon vagy a mentett környezeteken keresztül.</span><span class="sxs-lookup"><span data-stu-id="2eba8-164">Sensitive information such as subscription IDs and tenant IDs may still be exposed in stored information, through logs or saved contexts.</span></span> <span data-ttu-id="2eba8-165">A tárolt adatok törlésével kapcsolatban tekintse meg a [környezetek és hitelesítő adatok eltávolítását](#remove-azure-contexts-and-stored-credentials) ismertető szakaszt.</span><span class="sxs-lookup"><span data-stu-id="2eba8-165">To learn how to clear stored information, see the [Remove contexts and credentials](#remove-azure-contexts-and-stored-credentials) section.</span></span>

## <a name="remove-azure-contexts-and-stored-credentials"></a><span data-ttu-id="2eba8-166">Az Azure-környezetek és a tárolt hitelesítő adatok eltávolítása</span><span class="sxs-lookup"><span data-stu-id="2eba8-166">Remove Azure contexts and stored credentials</span></span>

<span data-ttu-id="2eba8-167">Azure-környezetek és hitelesítő adatok törlése:</span><span class="sxs-lookup"><span data-stu-id="2eba8-167">To clear Azure contexts and credentials:</span></span>

* <span data-ttu-id="2eba8-168">Jelentkezzen ki a fiókból a [Disconnect-AzAccount](/powershell/module/az.accounts/disconnect-azaccount) parancsmaggal.</span><span class="sxs-lookup"><span data-stu-id="2eba8-168">Sign out of an account with [Disconnect-AzAccount](/powershell/module/az.accounts/disconnect-azaccount).</span></span>
  <span data-ttu-id="2eba8-169">Bármely fiókból kijelentkezhet a fiók vagy a környezet megadásával:</span><span class="sxs-lookup"><span data-stu-id="2eba8-169">You can sign out of any account either by account or context:</span></span>

  ```azurepowershell-interactive
  Disconnect-AzAccount # Disconnect active account 
  Disconnect-AzAccount -Username "user@contoso.com" # Disconnect by account name

  Disconnect-AzAccount -ContextName "subscription2" # Disconnect by context name
  Disconnect-AzAccount -AzureContext $contextObject # Disconnect using context object information
  ```

  <span data-ttu-id="2eba8-170">A kapcsolat bontásakor a rendszer mindig eltávolítja a tárolt hitelesítési jogkivonatokat, és törli a leválasztott felhasználóhoz vagy környezethez társított mentett környezeteket.</span><span class="sxs-lookup"><span data-stu-id="2eba8-170">Disconnecting always removes stored authentication tokens and clears saved contexts associated with the disconnected user or context.</span></span>
* <span data-ttu-id="2eba8-171">Használja a [Clear-AzContext](/powershell/module/az.accounts/Clear-AzContext) parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="2eba8-171">Use [Clear-AzContext](/powershell/module/az.accounts/Clear-AzContext).</span></span> <span data-ttu-id="2eba8-172">Ez a parancsmag garantáltan mindig eltávolítja a tárolt környezeteket és hitelesítési jogkivonatokat, és a felhasználót is kilépteti.</span><span class="sxs-lookup"><span data-stu-id="2eba8-172">This cmdlet is guaranteed to always remove stored contexts and authentication tokens, and will also sign you out.</span></span>
* <span data-ttu-id="2eba8-173">Távolítson el egy környezetet a [Remove-AzContext](/powershell/module/az.accounts/remove-azcontext) parancsmaggal:</span><span class="sxs-lookup"><span data-stu-id="2eba8-173">Remove a context with [Remove-AzContext](/powershell/module/az.accounts/remove-azcontext):</span></span>
  
  ```azurepowershell-interactive
  Remove-AzContext -Name "mycontext" # Remove by name
  Get-AzContext -Name "mycontext" | Remove-AzContext # Remove by piping Azure context object
  ```

  <span data-ttu-id="2eba8-174">Ha eltávolítja az aktív környezetet, a rendszer bontja a kapcsolatot az Azure-ral, és Önnek újból hitelesítenie kell magát a `Connect-AzAccount` parancsmaggal.</span><span class="sxs-lookup"><span data-stu-id="2eba8-174">If you remove the active context, you will be disconnected from Azure and need to reauthenticate with `Connect-AzAccount`.</span></span>

## <a name="see-also"></a><span data-ttu-id="2eba8-175">Lásd még</span><span class="sxs-lookup"><span data-stu-id="2eba8-175">See also</span></span>

* [<span data-ttu-id="2eba8-176">Azure PowerShell-parancsmagok futtatása PowerShell-feladatokban</span><span class="sxs-lookup"><span data-stu-id="2eba8-176">Run Azure PowerShell cmdlets in PowerShell Jobs</span></span>](using-psjobs.md)
* [<span data-ttu-id="2eba8-177">Az Azure Active Directory terminológiája</span><span class="sxs-lookup"><span data-stu-id="2eba8-177">Azure Active Directory Terminology</span></span>](/azure/active-directory/fundamentals/active-directory-whatis#terminology)
* [<span data-ttu-id="2eba8-178">Az.Accounts referencia</span><span class="sxs-lookup"><span data-stu-id="2eba8-178">Az.Accounts reference</span></span>](/powershell/module/az.accounts)
