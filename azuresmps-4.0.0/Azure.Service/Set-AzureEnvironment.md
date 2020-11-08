---
external help file: Microsoft.WindowsAzure.Commands.Profile.dll-Help.xml
ms.assetid: 1094497D-2CBE-41DF-9ED1-8E7D3F14B05A
online version: ''
schema: 2.0.0
ms.openlocfilehash: 82bd806d35f36a07958f2bdeeeda42853cd453b9
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015967"
---
# <span data-ttu-id="4505f-101">Set-AzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="4505f-101">Set-AzureEnvironment</span></span>

## <span data-ttu-id="4505f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="4505f-102">SYNOPSIS</span></span>
<span data-ttu-id="4505f-103">Az Azure-környezet tulajdonságainak módosítása</span><span class="sxs-lookup"><span data-stu-id="4505f-103">Changes the properties of an Azure environment.</span></span>

## <span data-ttu-id="4505f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="4505f-104">SYNTAX</span></span>

```
Set-AzureEnvironment -Name <String> [-PublishSettingsFileUrl <String>] [-ServiceEndpoint <String>]
 [-ManagementPortalUrl <String>] [-StorageEndpoint <String>] [-ActiveDirectoryEndpoint <String>]
 [-ResourceManagerEndpoint <String>] [-GalleryEndpoint <String>]
 [-ActiveDirectoryServiceEndpointResourceId <String>] [-GraphEndpoint <String>]
 [-AzureKeyVaultDnsSuffix <String>] [-AzureKeyVaultServiceEndpointResourceId <String>]
 [-TrafficManagerDnsSuffix <String>] [-SqlDatabaseDnsSuffix <String>] [-EnableAdfsAuthentication]
 [-AdTenant <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="4505f-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="4505f-105">DESCRIPTION</span></span>
<span data-ttu-id="4505f-106">A **set-AzureEnvironment** parancsmag egy Azure-környezet tulajdonságait módosítja.</span><span class="sxs-lookup"><span data-stu-id="4505f-106">The **Set-AzureEnvironment** cmdlet changes the properties of an Azure environment.</span></span>
<span data-ttu-id="4505f-107">Egy olyan objektumot ad eredményül, amely a környezetet jelképezi az új tulajdonság értékeivel.</span><span class="sxs-lookup"><span data-stu-id="4505f-107">It returns an object that represents the environment with its new property values.</span></span>
<span data-ttu-id="4505f-108">A **Name** paraméterrel megadhatja a környezetet és a többi paramétert a tulajdonság értékeinek módosításához.</span><span class="sxs-lookup"><span data-stu-id="4505f-108">Use the **Name** parameter to identify the environment and the other parameters to change property values.</span></span>
<span data-ttu-id="4505f-109">Az Azure-környezet nevének módosításához a **set-AzureEnvironment** nem használható.</span><span class="sxs-lookup"><span data-stu-id="4505f-109">You cannot use **Set-AzureEnvironment** to change the name of an Azure environment.</span></span>

<span data-ttu-id="4505f-110">Azure-környezet: a Microsoft Azure független központi üzembe állítása, például a AzureCloud a globális Azure-és a AzureChinaCloud által üzemeltetett Azure-alapú 21Vianet Kínában.</span><span class="sxs-lookup"><span data-stu-id="4505f-110">An Azure environment an independent deployment of Microsoft Azure, such as AzureCloud for global Azure and AzureChinaCloud for Azure operated by 21Vianet in China.</span></span>
<span data-ttu-id="4505f-111">A helyszíni Azure-környezeteket az Azure Pack és a WAPack parancsmagok használatával is létrehozhatja.</span><span class="sxs-lookup"><span data-stu-id="4505f-111">You can also create on-premises Azure environments by using Azure Pack and the WAPack cmdlets.</span></span>
<span data-ttu-id="4505f-112">További tudnivalókat az [Azure Pack (csomag](https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx) ) című témakörben talál https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx) .</span><span class="sxs-lookup"><span data-stu-id="4505f-112">For more information, see [Azure Pack](https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx) (https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx).</span></span>

<span data-ttu-id="4505f-113">Megjegyzés: ne módosítsa a AzureCloud vagy a AzureChinaCloud környezet tulajdonságait.</span><span class="sxs-lookup"><span data-stu-id="4505f-113">NOTE:  Do not change the properties of the AzureCloud or AzureChinaCloud environments.</span></span>
<span data-ttu-id="4505f-114">Ezzel a parancsmaggal módosíthatja a létrehozott privát környezetek értékét.</span><span class="sxs-lookup"><span data-stu-id="4505f-114">Use this cmdlet to change the values of private environments that you create.</span></span>

## <span data-ttu-id="4505f-115">Példák</span><span class="sxs-lookup"><span data-stu-id="4505f-115">EXAMPLES</span></span>

### <span data-ttu-id="4505f-116">Példa 1: környezeti tulajdonságok módosítása</span><span class="sxs-lookup"><span data-stu-id="4505f-116">Example 1: Change environment properties</span></span>
```
PS C:\> Set-AzureEnvironment -Name ContosoEnv -PublishSettingsFileUrl "https://contoso.com" -StorageEndpoint "contoso.com"
```

<span data-ttu-id="4505f-117">Ez a parancs megváltoztatja az ContosoEnv környezet **PublishSettingsFileUrl** és **StorageEndpoint** tulajdonságainak értékét.</span><span class="sxs-lookup"><span data-stu-id="4505f-117">This command changes the values of the **PublishSettingsFileUrl** and **StorageEndpoint** properties of the ContosoEnv environment.</span></span>

## <span data-ttu-id="4505f-118">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="4505f-118">PARAMETERS</span></span>

### <span data-ttu-id="4505f-119">-ActiveDirectoryEndpoint</span><span class="sxs-lookup"><span data-stu-id="4505f-119">-ActiveDirectoryEndpoint</span></span>
<span data-ttu-id="4505f-120">Az Azure Active Directory-hitelesítés végpontját a megadott értékre módosítja.</span><span class="sxs-lookup"><span data-stu-id="4505f-120">Changes the endpoint for Azure Active Directory authentication to the specified value.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AdEndpointUrl, ActiveDirectory, ActiveDirectoryAuthority

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4505f-121">-ActiveDirectoryServiceEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="4505f-121">-ActiveDirectoryServiceEndpointResourceId</span></span>
<span data-ttu-id="4505f-122">Annak a kezelési API-nek az erőforrás-AZONOSÍTÓját adja meg, amelynek az elérését az Azure Active Directory kezeli.</span><span class="sxs-lookup"><span data-stu-id="4505f-122">Specifies the resource ID of a management API whose access is managed by Azure Active Directory.</span></span>

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

### <span data-ttu-id="4505f-123">-AdTenant</span><span class="sxs-lookup"><span data-stu-id="4505f-123">-AdTenant</span></span>
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

### <span data-ttu-id="4505f-124">-AzureKeyVaultDnsSuffix</span><span class="sxs-lookup"><span data-stu-id="4505f-124">-AzureKeyVaultDnsSuffix</span></span>
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

### <span data-ttu-id="4505f-125">-AzureKeyVaultServiceEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="4505f-125">-AzureKeyVaultServiceEndpointResourceId</span></span>
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

### <span data-ttu-id="4505f-126">-EnableAdfsAuthentication</span><span class="sxs-lookup"><span data-stu-id="4505f-126">-EnableAdfsAuthentication</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: OnPremise

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4505f-127">-GalleryEndpoint</span><span class="sxs-lookup"><span data-stu-id="4505f-127">-GalleryEndpoint</span></span>
<span data-ttu-id="4505f-128">Az Azure Resource Manager-gyűjtemény végpontját a megadott értékre módosítja.</span><span class="sxs-lookup"><span data-stu-id="4505f-128">Changes the endpoint for the Azure Resource Manager gallery to the specified value.</span></span>
<span data-ttu-id="4505f-129">A gyűjtemény végpontja az erőforráscsoport-gyűjtemény sablonjainak a helye.</span><span class="sxs-lookup"><span data-stu-id="4505f-129">The gallery endpoint is the location for resource group gallery templates.</span></span>
<span data-ttu-id="4505f-130">Az Azure Resource groups és a Gallery sablonjairól a [Get-AzureResourceGroupGalleryTemplate](https://go.microsoft.com/fwlink/?LinkID=393052)című súgótémakörben talál további információt.</span><span class="sxs-lookup"><span data-stu-id="4505f-130">For more information about Azure resource groups and gallery templates, see the help topic for [Get-AzureResourceGroupGalleryTemplate](https://go.microsoft.com/fwlink/?LinkID=393052).</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Gallery, GalleryUrl

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4505f-131">-GraphEndpoint</span><span class="sxs-lookup"><span data-stu-id="4505f-131">-GraphEndpoint</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: Graph, GraphUrl

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4505f-132">-ManagementPortalUrl</span><span class="sxs-lookup"><span data-stu-id="4505f-132">-ManagementPortalUrl</span></span>
<span data-ttu-id="4505f-133">A megadott értékre módosítja az Azure felügyeleti portál URL-címét.</span><span class="sxs-lookup"><span data-stu-id="4505f-133">Changes the URL of the Azure Management Portal to the specified value.</span></span>

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

### <span data-ttu-id="4505f-134">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="4505f-134">-Name</span></span>
<span data-ttu-id="4505f-135">A módosult környezet azonosítása.</span><span class="sxs-lookup"><span data-stu-id="4505f-135">Identifies the environment that is being changed.</span></span>
<span data-ttu-id="4505f-136">Ehhez a paraméterhez szükség van.</span><span class="sxs-lookup"><span data-stu-id="4505f-136">This parameter is required.</span></span>
<span data-ttu-id="4505f-137">A paraméter értéke megkülönbözteti a kis-és nagybetűket.</span><span class="sxs-lookup"><span data-stu-id="4505f-137">The parameter value is case-sensitive.</span></span>
<span data-ttu-id="4505f-138">A helyettesítő karakterek nem engedélyezettek.</span><span class="sxs-lookup"><span data-stu-id="4505f-138">Wildcard characters are not permitted.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4505f-139">-Profil</span><span class="sxs-lookup"><span data-stu-id="4505f-139">-Profile</span></span>
<span data-ttu-id="4505f-140">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="4505f-140">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="4505f-141">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="4505f-141">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="4505f-142">-PublishSettingsFileUrl</span><span class="sxs-lookup"><span data-stu-id="4505f-142">-PublishSettingsFileUrl</span></span>
<span data-ttu-id="4505f-143">A megadott környezetben módosítsa a közzétételi beállítások URL-címét.</span><span class="sxs-lookup"><span data-stu-id="4505f-143">Changes the URL for publish settings files in the specified environment.</span></span>
<span data-ttu-id="4505f-144">Az Azure közzétételi beállítások fájlja olyan XML-fájl, amely információkat tartalmaz a fiókjával és egy olyan felügyeleti tanúsítvánnyal, amely lehetővé teszi a Windows PowerShell számára az Azure-fiókjába való bejelentkezést az Ön nevében.</span><span class="sxs-lookup"><span data-stu-id="4505f-144">An Azure publish settings file is an XML file that contains information about your account and a management certificate that allows Windows PowerShell to sign into your Azure account on your behalf.</span></span>

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

### <span data-ttu-id="4505f-145">-ResourceManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="4505f-145">-ResourceManagerEndpoint</span></span>
<span data-ttu-id="4505f-146">Módosítja az Azure Resource Manager-adatok végpontját, például a fiókhoz társított erőforráscsoportok adatait.</span><span class="sxs-lookup"><span data-stu-id="4505f-146">Changes the endpoint for Azure Resource Manager data, including data about resource groups associated with the account.</span></span>
<span data-ttu-id="4505f-147">Az Azure Resource Managerről az [Azure Resource Manager parancsmagok](https://go.microsoft.com/fwlink/?LinkID=394765)  ( https://go.microsoft.com/fwlink/?LinkID=394765) és a [Windows PowerShell használata az erőforrás-kezelővel](https://go.microsoft.com/fwlink/?LinkID=394767)  című témakörben olvashat bővebben https://go.microsoft.com/fwlink/?LinkID=394767) .</span><span class="sxs-lookup"><span data-stu-id="4505f-147">For more information about Azure Resource Manager, see [Azure Resource Manager Cmdlets](https://go.microsoft.com/fwlink/?LinkID=394765)  (https://go.microsoft.com/fwlink/?LinkID=394765) and [Using Windows PowerShell with Resource Manager](https://go.microsoft.com/fwlink/?LinkID=394767)  (https://go.microsoft.com/fwlink/?LinkID=394767).</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceManager, ResourceManagerUrl

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4505f-148">-ServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="4505f-148">-ServiceEndpoint</span></span>
<span data-ttu-id="4505f-149">Módosítja az Azure szolgáltatás végpontjának URL-címét a megadott környezetben.</span><span class="sxs-lookup"><span data-stu-id="4505f-149">Changes the URL of the Azure service endpoint in the specified environment.</span></span>
<span data-ttu-id="4505f-150">Az Azure szolgáltatás végpontja azt határozza meg, hogy az alkalmazást a 21Vianet által Kínában üzemeltetett globális Azure platform, illetve egy privát Azure-példány kezeli-e.</span><span class="sxs-lookup"><span data-stu-id="4505f-150">The Azure service endpoint determines whether your application is managed by the global Azure platform, Azure operated by 21Vianet in China, or a private Azure installation.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ServiceManagement, ServiceManagementUrl

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4505f-151">-SqlDatabaseDnsSuffix</span><span class="sxs-lookup"><span data-stu-id="4505f-151">-SqlDatabaseDnsSuffix</span></span>
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

### <span data-ttu-id="4505f-152">-StorageEndpoint</span><span class="sxs-lookup"><span data-stu-id="4505f-152">-StorageEndpoint</span></span>
<span data-ttu-id="4505f-153">Módosítja a tárolási szolgáltatások alapértelmezett végpontját a megadott környezetben.</span><span class="sxs-lookup"><span data-stu-id="4505f-153">Changes the default endpoint of storage services in the specified environment.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: StorageEndpointSuffix

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4505f-154">-TrafficManagerDnsSuffix</span><span class="sxs-lookup"><span data-stu-id="4505f-154">-TrafficManagerDnsSuffix</span></span>
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

### <span data-ttu-id="4505f-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4505f-155">CommonParameters</span></span>
<span data-ttu-id="4505f-156">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="4505f-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4505f-157">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4505f-157">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4505f-158">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="4505f-158">INPUTS</span></span>

### <span data-ttu-id="4505f-159">Nincs</span><span class="sxs-lookup"><span data-stu-id="4505f-159">None</span></span>
<span data-ttu-id="4505f-160">A parancsmagot tulajdonság nevében, de nem érték szerint is beírhatja.</span><span class="sxs-lookup"><span data-stu-id="4505f-160">You can pipe input to this cmdlet by property name, but not by value.</span></span>

## <span data-ttu-id="4505f-161">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4505f-161">OUTPUTS</span></span>

### <span data-ttu-id="4505f-162">Microsoft. WindowsAzure. commands. Utilities. Common. WindowsAzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="4505f-162">Microsoft.WindowsAzure.Commands.Utilities.Common.WindowsAzureEnvironment</span></span>

## <span data-ttu-id="4505f-163">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="4505f-163">NOTES</span></span>

## <span data-ttu-id="4505f-164">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4505f-164">RELATED LINKS</span></span>

[<span data-ttu-id="4505f-165">Add-AzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="4505f-165">Add-AzureEnvironment</span></span>](./Add-AzureEnvironment.md)

[<span data-ttu-id="4505f-166">Get-AzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="4505f-166">Get-AzureEnvironment</span></span>](./Get-AzureEnvironment.md)

[<span data-ttu-id="4505f-167">Remove-AzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="4505f-167">Remove-AzureEnvironment</span></span>](./Remove-AzureEnvironment.md)


