---
external help file: Microsoft.WindowsAzure.Commands.Profile.dll-Help.xml
ms.assetid: 6185C6BA-460E-4EEA-B1EF-CD67629AA75E
online version: ''
schema: 2.0.0
ms.openlocfilehash: 51c20ef378cd2629ea96f236339a97172fb3038e
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015950"
---
# <span data-ttu-id="b3504-101">Set-AzureSubscription</span><span class="sxs-lookup"><span data-stu-id="b3504-101">Set-AzureSubscription</span></span>

## <span data-ttu-id="b3504-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b3504-102">SYNOPSIS</span></span>
<span data-ttu-id="b3504-103">Azure-előfizetés módosítása</span><span class="sxs-lookup"><span data-stu-id="b3504-103">Changes an Azure subscription.</span></span>

## <span data-ttu-id="b3504-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b3504-104">SYNTAX</span></span>

### <span data-ttu-id="b3504-105">UpdateSubscriptionByIdParameterSetName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="b3504-105">UpdateSubscriptionByIdParameterSetName (Default)</span></span>
```
Set-AzureSubscription -SubscriptionId <String> [-Certificate <X509Certificate2>] [-ServiceEndpoint <String>]
 [-ResourceManagerEndpoint <String>] [-CurrentStorageAccountName <String>] [-Context <AzureStorageContext>]
 [-Environment <String>] [-PassThru] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="b3504-106">UpdateSubscriptionByNameParameterSetName</span><span class="sxs-lookup"><span data-stu-id="b3504-106">UpdateSubscriptionByNameParameterSetName</span></span>
```
Set-AzureSubscription -SubscriptionName <String> [-Certificate <X509Certificate2>] [-ServiceEndpoint <String>]
 [-ResourceManagerEndpoint <String>] [-CurrentStorageAccountName <String>] [-Context <AzureStorageContext>]
 [-Environment <String>] [-PassThru] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="b3504-107">AddSubscriptionParameterSetName</span><span class="sxs-lookup"><span data-stu-id="b3504-107">AddSubscriptionParameterSetName</span></span>
```
Set-AzureSubscription -SubscriptionName <String> -SubscriptionId <String> -Certificate <X509Certificate2>
 [-ServiceEndpoint <String>] [-ResourceManagerEndpoint <String>] [-CurrentStorageAccountName <String>]
 [-Context <AzureStorageContext>] [-Environment <String>] [-PassThru] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="b3504-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="b3504-108">DESCRIPTION</span></span>
<span data-ttu-id="b3504-109">A **set-AzureSubscription** parancsmag az Azure-előfizetés objektum tulajdonságait hozza létre és módosítja.</span><span class="sxs-lookup"><span data-stu-id="b3504-109">The **Set-AzureSubscription** cmdlet establishes and changes the properties of an Azure subscription object.</span></span>
<span data-ttu-id="b3504-110">Ezzel a parancsmaggal olyan Azure-előfizetésben dolgozhat, amely nem az alapértelmezett előfizetése, illetve módosíthatja az aktuális tárterület-fiókot.</span><span class="sxs-lookup"><span data-stu-id="b3504-110">You can use this cmdlet to work in an Azure subscription that is not your default subscription or to change your current storage account.</span></span>
<span data-ttu-id="b3504-111">Az aktuális és az alapértelmezett előfizetésekről a **Select-AzureSubscription** parancsmag című témakörben olvashat bővebben.</span><span class="sxs-lookup"><span data-stu-id="b3504-111">For information about current and default subscriptions, see the **Select-AzureSubscription** cmdlet.</span></span>

<span data-ttu-id="b3504-112">Ez a parancsmag Azure-előfizetéses objektumon működik, és nem a tényleges Azure-előfizetése.</span><span class="sxs-lookup"><span data-stu-id="b3504-112">This cmdlet operates on an Azure subscription object, not your actual Azure subscription.</span></span>
<span data-ttu-id="b3504-113">Azure-előfizetés létrehozásához és létrehozásához keresse fel az [Azure portált](https://azure.microsoft.com/) ( https://azure.microsoft.com/) .</span><span class="sxs-lookup"><span data-stu-id="b3504-113">To create and provision an Azure subscription, visit the [Azure Portal](https://azure.microsoft.com/) (https://azure.microsoft.com/).</span></span>

<span data-ttu-id="b3504-114">Ez a parancsmag azokat az előfizetési adatfájlokat módosítja, amelyeket a **Add-AzureAccount** vagy az **import-AzurePublishSettingsFile** parancsmaggal létrehozott, ha Azure-fiókot szeretne felvenni a Windows powershellbe.</span><span class="sxs-lookup"><span data-stu-id="b3504-114">This cmdlet changes the data in the subscription data file that you create when you use the **Add-AzureAccount** or **Import-AzurePublishSettingsFile** cmdlet to add an Azure account to Windows PowerShell.</span></span>

<span data-ttu-id="b3504-115">Ez a témakör a Microsoft Azure PowerShell modul 0.8.10 verziójában található parancsmagot ismerteti.</span><span class="sxs-lookup"><span data-stu-id="b3504-115">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="b3504-116">A használt modul verziójának beszerzéséhez az Azure PowerShell konzolon írja be a következőt: `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="b3504-116">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

## <span data-ttu-id="b3504-117">Példák</span><span class="sxs-lookup"><span data-stu-id="b3504-117">EXAMPLES</span></span>

### <span data-ttu-id="b3504-118">Példa 1: meglévő subscription1 módosítása</span><span class="sxs-lookup"><span data-stu-id="b3504-118">Example 1: Change an existing subscription1</span></span>
```
C:\PS> $thumbprint = <Thumbprint-2>
C:\PS> $differentCert = Get-Item cert:\\CurrentUser\My\$thumbprint 
C:\PS> Set-AzureSubscription -SubscriptionName ContosoEngineering -Certificate $differentCert
```

<span data-ttu-id="b3504-119">Ez a példa a ContosoEngineering nevű előfizetés tanúsítványát módosítja.</span><span class="sxs-lookup"><span data-stu-id="b3504-119">This example changes the certificate for the subscription named ContosoEngineering.</span></span>

### <span data-ttu-id="b3504-120">2. példa: a szolgáltatás végpontjának módosítása</span><span class="sxs-lookup"><span data-stu-id="b3504-120">Example 2: Change the service endpoint</span></span>
```
C:\PS> Set-AzureSubscription -SubscriptionName ContosoEngineering -ServiceEndpoint "https://management.core.contoso.com"
```

<span data-ttu-id="b3504-121">Ez a parancs hozzáadja vagy módosítja az ContosoEngineering-előfizetés egyéni szolgáltatási végpontját.</span><span class="sxs-lookup"><span data-stu-id="b3504-121">This command adds or changes a custom service endpoint for the ContosoEngineering subscription.</span></span>

### <span data-ttu-id="b3504-122">3. példa: tulajdonságérték törlése</span><span class="sxs-lookup"><span data-stu-id="b3504-122">Example 3: Clear property values</span></span>
```
C:\PS> Set-AzureSubscription -SubscriptionName ContosoEngineering -Certificate $null -ResourceManagerEndpoint $Null
```

<span data-ttu-id="b3504-123">A parancs a tanúsítvány és a ResourceManagerEndpoint tulajdonság értékét NULL értékűre ($Null) állítja be.</span><span class="sxs-lookup"><span data-stu-id="b3504-123">This command sets the values of the Certificate and ResourceManagerEndpoint properties to null ($Null).</span></span>
<span data-ttu-id="b3504-124">Ezzel a beállítással a többi beállítás módosítása nélkül törölheti a tulajdonságok értékét.</span><span class="sxs-lookup"><span data-stu-id="b3504-124">This clears the values of those properties without changing other settings.</span></span>

### <span data-ttu-id="b3504-125">4. példa: alternatív előfizetési adatfájl használata</span><span class="sxs-lookup"><span data-stu-id="b3504-125">Example 4: Use an alternate subscription data file</span></span>
```
C:\PS> Set-AzureSubscription -SubscriptionName ContosoFinance -SubscriptionDataFile C:\Azure\SubscriptionData.xml -CurrentStorageAccount ContosoStorage01
```

<span data-ttu-id="b3504-126">Ez a parancs megváltoztatja a ContosoFinance-előfizetés jelenlegi tárolási fiókját a ContosoStorage01.</span><span class="sxs-lookup"><span data-stu-id="b3504-126">This command changes the current storage account of the ContosoFinance subscription to ContosoStorage01.</span></span>
<span data-ttu-id="b3504-127">A parancs a **SubscriptionDataFile** paraméterrel módosítja az adatC:\Azure\SubscriptionData.xml-előfizetés adatfájlban lévő adattípust.</span><span class="sxs-lookup"><span data-stu-id="b3504-127">The command uses the **SubscriptionDataFile** parameter to change the data in the C:\Azure\SubscriptionData.xml subscription data file.</span></span>
<span data-ttu-id="b3504-128">A **set-AzureSubscription** alapértelmezés szerint az alapértelmezett előfizetési adatfájlt használja a központi felhasználói profilban.</span><span class="sxs-lookup"><span data-stu-id="b3504-128">By default, **Set-AzureSubscription** uses the default subscription data file in your roaming user profile.</span></span>

## <span data-ttu-id="b3504-129">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b3504-129">PARAMETERS</span></span>

### <span data-ttu-id="b3504-130">-Tanúsítvány</span><span class="sxs-lookup"><span data-stu-id="b3504-130">-Certificate</span></span>
```yaml
Type: X509Certificate2
Parameter Sets: UpdateSubscriptionByIdParameterSetName, UpdateSubscriptionByNameParameterSetName
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: X509Certificate2
Parameter Sets: AddSubscriptionParameterSetName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b3504-131">-Környezet</span><span class="sxs-lookup"><span data-stu-id="b3504-131">-Context</span></span>
```yaml
Type: AzureStorageContext
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b3504-132">-CurrentStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="b3504-132">-CurrentStorageAccountName</span></span>
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

### <span data-ttu-id="b3504-133">-Környezet</span><span class="sxs-lookup"><span data-stu-id="b3504-133">-Environment</span></span>
<span data-ttu-id="b3504-134">Azure-környezetet ad meg.</span><span class="sxs-lookup"><span data-stu-id="b3504-134">Specifies an Azure environment.</span></span>

<span data-ttu-id="b3504-135">Azure-környezet: a Microsoft Azure független központi üzembe állítása, például a AzureCloud a globális Azure-és a AzureChinaCloud által üzemeltetett Azure-alapú 21Vianet Kínában.</span><span class="sxs-lookup"><span data-stu-id="b3504-135">An Azure environment an independent deployment of Microsoft Azure, such as AzureCloud for global Azure and AzureChinaCloud for Azure operated by 21Vianet in China.</span></span>
<span data-ttu-id="b3504-136">A helyszíni Azure-környezeteket az Azure Pack és a WAPack parancsmagok használatával is létrehozhatja.</span><span class="sxs-lookup"><span data-stu-id="b3504-136">You can also create on-premises Azure environments by using Azure Pack and the WAPack cmdlets.</span></span>
<span data-ttu-id="b3504-137">További tudnivalókat az [Azure Pack (csomag](https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx)  ) című témakörben talál https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx) .</span><span class="sxs-lookup"><span data-stu-id="b3504-137">For more information, see [Azure Pack](https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx)  (https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx).</span></span>

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

### <span data-ttu-id="b3504-138">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b3504-138">-PassThru</span></span>
<span data-ttu-id="b3504-139">A parancs eredményét $True, ha a parancs sikerül, és a $False sikertelen.</span><span class="sxs-lookup"><span data-stu-id="b3504-139">Returns $True if the command succeeds and $False if it fails.</span></span>
<span data-ttu-id="b3504-140">Ez a parancsmag alapértelmezés szerint nem ad vissza semmilyen eredményt.</span><span class="sxs-lookup"><span data-stu-id="b3504-140">By default, this cmdlet does not return any output.</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b3504-141">-Profil</span><span class="sxs-lookup"><span data-stu-id="b3504-141">-Profile</span></span>
<span data-ttu-id="b3504-142">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="b3504-142">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="b3504-143">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="b3504-143">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="b3504-144">-ResourceManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="b3504-144">-ResourceManagerEndpoint</span></span>
<span data-ttu-id="b3504-145">Az Azure Resource Manager-adatok végpontját adja meg, például a fiókhoz társított erőforráscsoportok adatait.</span><span class="sxs-lookup"><span data-stu-id="b3504-145">Specifies the endpoint for Azure Resource Manager data, including data about resource groups associated with the account.</span></span>
<span data-ttu-id="b3504-146">Az Azure Resource Managerről az [Azure Resource Manager parancsmagok](https://go.microsoft.com/fwlink/?LinkID=394765)  ( https://go.microsoft.com/fwlink/?LinkID=394765) és a [Windows PowerShell használata az erőforrás-kezelővel](https://go.microsoft.com/fwlink/?LinkID=394767)  című témakörben olvashat bővebben https://go.microsoft.com/fwlink/?LinkID=394767) .</span><span class="sxs-lookup"><span data-stu-id="b3504-146">For more information about Azure Resource Manager, see [Azure Resource Manager Cmdlets](https://go.microsoft.com/fwlink/?LinkID=394765)  (https://go.microsoft.com/fwlink/?LinkID=394765) and [Using Windows PowerShell with Resource Manager](https://go.microsoft.com/fwlink/?LinkID=394767)  (https://go.microsoft.com/fwlink/?LinkID=394767).</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b3504-147">-ServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="b3504-147">-ServiceEndpoint</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b3504-148">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="b3504-148">-SubscriptionId</span></span>
```yaml
Type: String
Parameter Sets: UpdateSubscriptionByIdParameterSetName, AddSubscriptionParameterSetName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b3504-149">-SubscriptionName</span><span class="sxs-lookup"><span data-stu-id="b3504-149">-SubscriptionName</span></span>
```yaml
Type: String
Parameter Sets: UpdateSubscriptionByNameParameterSetName, AddSubscriptionParameterSetName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b3504-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b3504-150">CommonParameters</span></span>
<span data-ttu-id="b3504-151">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b3504-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b3504-152">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b3504-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b3504-153">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b3504-153">INPUTS</span></span>

### <span data-ttu-id="b3504-154">Nincs</span><span class="sxs-lookup"><span data-stu-id="b3504-154">None</span></span>
<span data-ttu-id="b3504-155">A parancsmagot tulajdonság nevében, de nem érték szerint is beírhatja.</span><span class="sxs-lookup"><span data-stu-id="b3504-155">You can pipe input to this cmdlet by property name, but not by value.</span></span>

## <span data-ttu-id="b3504-156">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b3504-156">OUTPUTS</span></span>

### <span data-ttu-id="b3504-157">Nincs vagy System. Boolean</span><span class="sxs-lookup"><span data-stu-id="b3504-157">None or System.Boolean</span></span>
<span data-ttu-id="b3504-158">A *PassThru* paraméter használatakor ez a parancsmag logikai értéket ad eredményül.</span><span class="sxs-lookup"><span data-stu-id="b3504-158">When you use the *PassThru* parameter, this cmdlet returns a Boolean value.</span></span>
<span data-ttu-id="b3504-159">Ez a parancsmag alapértelmezés szerint nem ad vissza semmilyen eredményt.</span><span class="sxs-lookup"><span data-stu-id="b3504-159">By default, this cmdlet does not return any output.</span></span>

## <span data-ttu-id="b3504-160">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b3504-160">NOTES</span></span>

## <span data-ttu-id="b3504-161">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b3504-161">RELATED LINKS</span></span>

[<span data-ttu-id="b3504-162">Add-AzureAccount</span><span class="sxs-lookup"><span data-stu-id="b3504-162">Add-AzureAccount</span></span>](./Add-AzureAccount.md)

[<span data-ttu-id="b3504-163">Get-AzureSubscription</span><span class="sxs-lookup"><span data-stu-id="b3504-163">Get-AzureSubscription</span></span>](./Get-AzureSubscription.md)

[<span data-ttu-id="b3504-164">Importálás – AzurePublishSettingsFile</span><span class="sxs-lookup"><span data-stu-id="b3504-164">Import-AzurePublishSettingsFile</span></span>](./Import-AzurePublishSettingsFile.md)

[<span data-ttu-id="b3504-165">Remove-AzureSubscription</span><span class="sxs-lookup"><span data-stu-id="b3504-165">Remove-AzureSubscription</span></span>](./Remove-AzureSubscription.md)

[<span data-ttu-id="b3504-166">Select-AzureSubscription</span><span class="sxs-lookup"><span data-stu-id="b3504-166">Select-AzureSubscription</span></span>](./Select-AzureSubscription.md)


