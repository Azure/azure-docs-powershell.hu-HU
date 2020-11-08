---
external help file: Microsoft.WindowsAzure.Commands.Profile.dll-Help.xml
ms.assetid: 03EAFFB2-EA64-4227-A33B-D24EB4A75F71
online version: ''
schema: 2.0.0
ms.openlocfilehash: ac88bc2494bad975c6169262edd05c7b821061bb
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016396"
---
# <span data-ttu-id="30c21-101">Add-AzureAccount</span><span class="sxs-lookup"><span data-stu-id="30c21-101">Add-AzureAccount</span></span>

## <span data-ttu-id="30c21-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="30c21-102">SYNOPSIS</span></span>
<span data-ttu-id="30c21-103">Hozzáadja az Azure-fiókot a Windows PowerShellhez.</span><span class="sxs-lookup"><span data-stu-id="30c21-103">Adds the Azure account to Windows PowerShell.</span></span>

## <span data-ttu-id="30c21-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="30c21-104">SYNTAX</span></span>

### <span data-ttu-id="30c21-105">Felhasználó (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="30c21-105">User (Default)</span></span>
```
Add-AzureAccount [-Environment <String>] [-Credential <PSCredential>] [-Tenant <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="30c21-106">ServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="30c21-106">ServicePrincipal</span></span>
```
Add-AzureAccount [-Environment <String>] -Credential <PSCredential> [-ServicePrincipal] -Tenant <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="30c21-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="30c21-107">DESCRIPTION</span></span>
<span data-ttu-id="30c21-108">A **Add-AzureAccount** parancsmag az Azure-fiókját és a hozzájuk tartozó előfizetéseket is elérhetővé teszi a Windows PowerShellben.</span><span class="sxs-lookup"><span data-stu-id="30c21-108">The **Add-AzureAccount** cmdlet makes your Azure account and its subscriptions available in Windows PowerShell.</span></span>
<span data-ttu-id="30c21-109">Ez olyan, mint az Azure-fiókjába való bejelentkezés a Windows PowerShellben.</span><span class="sxs-lookup"><span data-stu-id="30c21-109">It's like logging into your Azure account in Windows PowerShell.</span></span>
<span data-ttu-id="30c21-110">Ha ki szeretne jelentkezni a fiókból, használja a **Remove-AzureAccount** parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="30c21-110">To log out of the account, use the **Remove-AzureAccount** cmdlet.</span></span>

<span data-ttu-id="30c21-111">A **AzureAccount** letölti az Azure-fiókjával kapcsolatos információkat, és egy előfizetési adatfájlba menti a központi felhasználói profilban.</span><span class="sxs-lookup"><span data-stu-id="30c21-111">**Add-AzureAccount** downloads information about your Azure account and saves it in a subscription data file in your roaming user profile.</span></span>
<span data-ttu-id="30c21-112">Egy hozzáférési tokent is kap, amely lehetővé teszi, hogy a Windows PowerShell hozzáférhessen az Azure-fiókjához az Ön nevében.</span><span class="sxs-lookup"><span data-stu-id="30c21-112">It also gets an access token that allows Windows PowerShell to access your Azure account on your behalf.</span></span>
<span data-ttu-id="30c21-113">Ha befejeződött a parancs, kezelheti az Azure-fiókját a Windows PowerShell segítségével.</span><span class="sxs-lookup"><span data-stu-id="30c21-113">When the command completes, you can manage your Azure account in Windows PowerShell.</span></span>

<span data-ttu-id="30c21-114">Az Azure-fiók kétféle módon érhető el a Windows PowerShellben.</span><span class="sxs-lookup"><span data-stu-id="30c21-114">There are two different ways to make your Azure account available to Windows PowerShell.</span></span>
<span data-ttu-id="30c21-115">Használhatja az **Add-AzureAccount** parancsmagot, amely az Azure Active Directoryt (Azure ad) hitelesítő (Azure ad) hozzáférési jogkivonatokat, illetve egy felügyeleti tanúsítványt használó **import-AzurePublishSettingsFile-** ot használ.</span><span class="sxs-lookup"><span data-stu-id="30c21-115">You can use the **Add-AzureAccount** cmdlet, which uses Azure Active Directory (Azure AD) authentication access tokens, or **Import-AzurePublishSettingsFile** , which uses a management certificate.</span></span>
<span data-ttu-id="30c21-116">A használati módszert a következő témakörben találhatja meg [: útmutató: csatlakozás az előfizetéshez](https://azure.microsoft.com/documentation/articles/install-configure-powershell) ( https://azure.microsoft.com/documentation/articles/install-configure-powershell/#Connect) .</span><span class="sxs-lookup"><span data-stu-id="30c21-116">For guidance on which method to use, see [How to: Connect to your subscription](https://azure.microsoft.com/documentation/articles/install-configure-powershell) (https://azure.microsoft.com/documentation/articles/install-configure-powershell/#Connect).</span></span>

<span data-ttu-id="30c21-117">A **AzureAccount** futtatásakor egy interaktív ablak jelenik meg, amely az Azure-fiókba való bejelentkezést kéri.</span><span class="sxs-lookup"><span data-stu-id="30c21-117">When you run **Add-AzureAccount** , it displays an interactive window that prompts you to sign into your Azure account.</span></span>
<span data-ttu-id="30c21-118">Ez a bejelentkezés addig érvényes, amíg lejár a hozzáférési jogkivonat.</span><span class="sxs-lookup"><span data-stu-id="30c21-118">This sign-in is valid until the access token expires.</span></span>
<span data-ttu-id="30c21-119">Ha lejár, a fiókjához való hozzáférést igénylő parancsmagokra kéri a **AzureAccount** ismételt futtatását.</span><span class="sxs-lookup"><span data-stu-id="30c21-119">When it expires, cmdlets that require access to your account prompt you to run **Add-AzureAccount** again.</span></span>

<span data-ttu-id="30c21-120">Ez a témakör a Microsoft Azure PowerShell modul 0.8.10 verziójában található parancsmagot ismerteti.</span><span class="sxs-lookup"><span data-stu-id="30c21-120">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="30c21-121">A használt modul verziójának beszerzéséhez az Azure PowerShell konzolon írja be a következőt: `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="30c21-121">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

## <span data-ttu-id="30c21-122">Példák</span><span class="sxs-lookup"><span data-stu-id="30c21-122">EXAMPLES</span></span>

### <span data-ttu-id="30c21-123">1. példa: fiók hozzáadása</span><span class="sxs-lookup"><span data-stu-id="30c21-123">Example 1: Add an account</span></span>
```
PS C:\> Add-AzureAccount
```

<span data-ttu-id="30c21-124">Ez a parancs Azure-fiókot ad hozzá a Windows PowerShellhez.</span><span class="sxs-lookup"><span data-stu-id="30c21-124">This command adds an Azure account to Windows PowerShell.</span></span>
<span data-ttu-id="30c21-125">Amikor futtatja a parancsot, a Windows megjelenik a fiók felhasználónevének és jelszavának megkereséséhez.</span><span class="sxs-lookup"><span data-stu-id="30c21-125">When you run the command, a windows pops up to request the user name and password of the account.</span></span>

### <span data-ttu-id="30c21-126">2. példa: alternatív előfizetési adatfájl használata</span><span class="sxs-lookup"><span data-stu-id="30c21-126">Example 2: Use an alternate subscription data file</span></span>
```
PS C:\> Add-AzureAccount -SubscriptionDataFile C:\Testing\SDF.xml
```

<span data-ttu-id="30c21-127">Ez a parancs a **SubscriptionDataFile** paramétert használva közvetlen **AzureAccount hoz létre** a fiókadatok tárolásához az alapértelmezett fájl helyett az C:\Testing\SDF.xml-fájlban.</span><span class="sxs-lookup"><span data-stu-id="30c21-127">This command uses the **SubscriptionDataFile** parameter to direct **Add-AzureAccount** to store the account data in the C:\Testing\SDF.xml file, instead of the default file.</span></span>

## <span data-ttu-id="30c21-128">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="30c21-128">PARAMETERS</span></span>

### <span data-ttu-id="30c21-129">-Hitelesítő adatok</span><span class="sxs-lookup"><span data-stu-id="30c21-129">-Credential</span></span>
```yaml
Type: PSCredential
Parameter Sets: User
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: PSCredential
Parameter Sets: ServicePrincipal
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30c21-130">-Környezet</span><span class="sxs-lookup"><span data-stu-id="30c21-130">-Environment</span></span>
<span data-ttu-id="30c21-131">Azure-környezetet ad meg.</span><span class="sxs-lookup"><span data-stu-id="30c21-131">Specifies an Azure environment.</span></span>

<span data-ttu-id="30c21-132">Azure-környezet: a Microsoft Azure független központi üzembe állítása, például a AzureCloud a globális Azure-és a AzureChinaCloud által üzemeltetett Azure-alapú 21Vianet Kínában.</span><span class="sxs-lookup"><span data-stu-id="30c21-132">An Azure environment an independent deployment of Microsoft Azure, such as AzureCloud for global Azure and AzureChinaCloud for Azure operated by 21Vianet in China.</span></span>
<span data-ttu-id="30c21-133">A helyszíni Azure-környezeteket az Azure Pack és a WAPack parancsmagok használatával is létrehozhatja.</span><span class="sxs-lookup"><span data-stu-id="30c21-133">You can also create on-premises Azure environments by using Azure Pack and the WAPack cmdlets.</span></span>
<span data-ttu-id="30c21-134">További tudnivalókat az [Azure Pack (csomag](https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx)  ) című témakörben talál https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx) .</span><span class="sxs-lookup"><span data-stu-id="30c21-134">For more information, see [Azure Pack](https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx)  (https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx).</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30c21-135">-Profil</span><span class="sxs-lookup"><span data-stu-id="30c21-135">-Profile</span></span>
<span data-ttu-id="30c21-136">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="30c21-136">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="30c21-137">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="30c21-137">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30c21-138">-ServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="30c21-138">-ServicePrincipal</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: ServicePrincipal
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30c21-139">-Bérlő</span><span class="sxs-lookup"><span data-stu-id="30c21-139">-Tenant</span></span>
```yaml
Type: String
Parameter Sets: User
Aliases: TenantId

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ServicePrincipal
Aliases: TenantId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30c21-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="30c21-140">CommonParameters</span></span>
<span data-ttu-id="30c21-141">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="30c21-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="30c21-142">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="30c21-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="30c21-143">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="30c21-143">INPUTS</span></span>

### <span data-ttu-id="30c21-144">Nincs</span><span class="sxs-lookup"><span data-stu-id="30c21-144">None</span></span>
<span data-ttu-id="30c21-145">Ehhez a parancsmaghoz nem tud bemeneti pipát</span><span class="sxs-lookup"><span data-stu-id="30c21-145">You cannot pipe input to this cmdlet</span></span>

## <span data-ttu-id="30c21-146">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="30c21-146">OUTPUTS</span></span>

### <span data-ttu-id="30c21-147">Nincs</span><span class="sxs-lookup"><span data-stu-id="30c21-147">None</span></span>
<span data-ttu-id="30c21-148">Ez a parancsmag nem ad vissza semmilyen eredményt.</span><span class="sxs-lookup"><span data-stu-id="30c21-148">This cmdlet does not return any output.</span></span>

## <span data-ttu-id="30c21-149">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="30c21-149">NOTES</span></span>
* <span data-ttu-id="30c21-150">Az **Add-AzureAccount** (és az Azure ad Authentication Method) az **import-AzurePublishSettings** (és a kezelési tanúsítvány módszerét) veszi figyelembe.</span><span class="sxs-lookup"><span data-stu-id="30c21-150">**Add-AzureAccount** (and the Azure AD authentication method) takes precedence over **Import-AzurePublishSettings** (and the management certificate method).</span></span> <span data-ttu-id="30c21-151">Ha a **AzureAccount** még egyszer használja a fiókjában, az Azure ad Authentication módszert használja, és a kezelési tanúsítványt figyelmen kívül hagyja.</span><span class="sxs-lookup"><span data-stu-id="30c21-151">If you use **Add-AzureAccount** even once on your account, the Azure AD authentication method is used and the management certificate is ignored.</span></span> <span data-ttu-id="30c21-152">Ha el szeretné távolítani az Azure AD tokent, és vissza szeretné állítani a felügyeleti tanúsítvány módszert, használja a **Remove-AzureAccount** parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="30c21-152">To remove the Azure AD token and restore the management certificate method, use the **Remove-AzureAccount** cmdlet.</span></span> <span data-ttu-id="30c21-153">További információért írja be a következőt: **Get-Help Remove-AzureAccount**.</span><span class="sxs-lookup"><span data-stu-id="30c21-153">For more information, type: **Get-Help Remove-AzureAccount**.</span></span>
* <span data-ttu-id="30c21-154">A hiba "a hitelesítő adatai lejártak".</span><span class="sxs-lookup"><span data-stu-id="30c21-154">The error, "Your credentials have expired.</span></span> <span data-ttu-id="30c21-155">Kérjük, hogy jelentkezzen be újra a Add-AzureAccount használatával. "</span><span class="sxs-lookup"><span data-stu-id="30c21-155">Please use Add-AzureAccount to log in again."</span></span> <span data-ttu-id="30c21-156">jelzi, hogy az Access-jogkivonat lejárt, és a Windows PowerShell nem fér hozzá az Azure-fiókjához.</span><span class="sxs-lookup"><span data-stu-id="30c21-156">indicates that your access token is expired and Windows PowerShell cannot access your Azure account.</span></span> <span data-ttu-id="30c21-157">Ha vissza szeretné állítani a fiókjához való hozzáférést, futtassa újra a **AzureAccount** .</span><span class="sxs-lookup"><span data-stu-id="30c21-157">To restore access to your account, run **Add-AzureAccount** again.</span></span>
* <span data-ttu-id="30c21-158">Az Azure PowerShell-fiók és az előfizetés-parancsmagok az előfizetési adatfájlból jutnak hozzá az adataihoz, nem az élő Azure-fiókból.</span><span class="sxs-lookup"><span data-stu-id="30c21-158">The Azure PowerShell account and subscription cmdlets get their data from the  subscription data file, not from the live Azure account.</span></span> <span data-ttu-id="30c21-159">Ha a Windows PowerShellen kívüli fiókját vagy előfizetéseit (például az Azure felügyeleti portál segítségével) módosítja, az előfizetési adatfájl frissítéséhez futtassa ismét a **Add-AzureAccount** .</span><span class="sxs-lookup"><span data-stu-id="30c21-159">If you change your account or subscriptions outside of Windows PowerShell, such as by using the Azure Management Portal, run **Add-AzureAccount** again to refresh the subscription data file.</span></span>

## <span data-ttu-id="30c21-160">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="30c21-160">RELATED LINKS</span></span>

[<span data-ttu-id="30c21-161">Add-AzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="30c21-161">Add-AzureEnvironment</span></span>](./Add-AzureEnvironment.md)

[<span data-ttu-id="30c21-162">Get-AzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="30c21-162">Get-AzureEnvironment</span></span>](./Get-AzureEnvironment.md)

[<span data-ttu-id="30c21-163">Importálás – AzurePublishSettingsFile</span><span class="sxs-lookup"><span data-stu-id="30c21-163">Import-AzurePublishSettingsFile</span></span>](./Import-AzurePublishSettingsFile.md)

[<span data-ttu-id="30c21-164">Get-AzureAccount</span><span class="sxs-lookup"><span data-stu-id="30c21-164">Get-AzureAccount</span></span>](./Get-AzureAccount.md)

[<span data-ttu-id="30c21-165">Remove-AzureAccount</span><span class="sxs-lookup"><span data-stu-id="30c21-165">Remove-AzureAccount</span></span>](./Remove-AzureAccount.md)


