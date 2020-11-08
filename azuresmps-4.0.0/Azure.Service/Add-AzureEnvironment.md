---
external help file: Microsoft.WindowsAzure.Commands.Profile.dll-Help.xml
ms.assetid: 6C435518-06EA-41B7-9585-44107B026FF1
online version: ''
schema: 2.0.0
ms.openlocfilehash: b04ceff5c4c49fe0e03e1e2c3da94c118323d653
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015730"
---
# <span data-ttu-id="c5c64-101">Add-AzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="c5c64-101">Add-AzureEnvironment</span></span>

## <span data-ttu-id="c5c64-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c5c64-102">SYNOPSIS</span></span>
<span data-ttu-id="c5c64-103">Azure-környezetet hoz létre.</span><span class="sxs-lookup"><span data-stu-id="c5c64-103">Creates an Azure environment.</span></span>

## <span data-ttu-id="c5c64-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c5c64-104">SYNTAX</span></span>

```
Add-AzureEnvironment -Name <String> [-PublishSettingsFileUrl <String>] [-ServiceEndpoint <String>]
 [-ManagementPortalUrl <String>] [-StorageEndpoint <String>] [-ActiveDirectoryEndpoint <String>]
 [-ResourceManagerEndpoint <String>] [-GalleryEndpoint <String>]
 [-ActiveDirectoryServiceEndpointResourceId <String>] [-GraphEndpoint <String>]
 [-AzureKeyVaultDnsSuffix <String>] [-AzureKeyVaultServiceEndpointResourceId <String>]
 [-TrafficManagerDnsSuffix <String>] [-SqlDatabaseDnsSuffix <String>] [-EnableAdfsAuthentication]
 [-AdTenant <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="c5c64-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="c5c64-105">DESCRIPTION</span></span>
<span data-ttu-id="c5c64-106">Az **Add-AzureEnvironment** parancsmag létrehoz egy új egyéni Azure-fiók környezetet, és a központi felhasználói profilba menti.</span><span class="sxs-lookup"><span data-stu-id="c5c64-106">The **Add-AzureEnvironment** cmdlet creates a new custom Azure account environment and saves it in your roaming user profile.</span></span>
<span data-ttu-id="c5c64-107">A parancsmag egy olyan objektumot ad eredményül, amely az új környezetet jelképezi.</span><span class="sxs-lookup"><span data-stu-id="c5c64-107">The cmdlet returns an object that represents the new environment.</span></span>
<span data-ttu-id="c5c64-108">A parancs befejeztével használhatja a környezetet a Windows PowerShellben.</span><span class="sxs-lookup"><span data-stu-id="c5c64-108">When the command completes, you can use the environment in Windows PowerShell.</span></span>

<span data-ttu-id="c5c64-109">Azure-környezet: a Microsoft Azure független központi üzembe állítása, például a AzureCloud a globális Azure-és a AzureChinaCloud által üzemeltetett Azure-alapú 21Vianet Kínában.</span><span class="sxs-lookup"><span data-stu-id="c5c64-109">An Azure environment an independent deployment of Microsoft Azure, such as AzureCloud for global Azure and AzureChinaCloud for Azure operated by 21Vianet in China.</span></span>
<span data-ttu-id="c5c64-110">A helyszíni Azure-környezeteket az Azure Pack és a WAPack parancsmagok használatával is létrehozhatja.</span><span class="sxs-lookup"><span data-stu-id="c5c64-110">You can also create on-premises Azure environments by using Azure Pack and the WAPack cmdlets.</span></span>
<span data-ttu-id="c5c64-111">További tudnivalókat az [Azure Pack (csomag](https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx) ) című témakörben talál https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx) .</span><span class="sxs-lookup"><span data-stu-id="c5c64-111">For more information, see [Azure Pack](https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx) (https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx).</span></span>

<span data-ttu-id="c5c64-112">A parancsmag csak a **Name** paramétert kötelező megadni.</span><span class="sxs-lookup"><span data-stu-id="c5c64-112">Only the **Name** parameter of this cmdlet is mandatory.</span></span>
<span data-ttu-id="c5c64-113">Ha kihagy egy paramétert, az értéke null ($Null), és a végpontot használó szolgáltatás nem működik megfelelően.</span><span class="sxs-lookup"><span data-stu-id="c5c64-113">If you omit a parameter, its value is null ($Null), and the service that uses that endpoint might not function properly.</span></span>
<span data-ttu-id="c5c64-114">Egy környezeti tulajdonság értékének hozzáadásához vagy módosításához használja a **set-AzureEnvironment** parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="c5c64-114">To add or change the value of an environment property, use the **Set-AzureEnvironment** cmdlet.</span></span>

<span data-ttu-id="c5c64-115">Megjegyzés: a környezet módosítása következtében a fiókja sikertelen lehet.</span><span class="sxs-lookup"><span data-stu-id="c5c64-115">NOTE: Changing your environment can cause your account to fail.</span></span>
<span data-ttu-id="c5c64-116">A környezetek általában csak tesztelésre vagy hibaelhárításra kerülnek.</span><span class="sxs-lookup"><span data-stu-id="c5c64-116">Typically, environments are added only for testing or troubleshooting.</span></span>

<span data-ttu-id="c5c64-117">Ez a témakör a Microsoft Azure PowerShell modul 0.8.10 verziójában található parancsmagot ismerteti.</span><span class="sxs-lookup"><span data-stu-id="c5c64-117">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="c5c64-118">A használt modul verziójának beszerzéséhez az Azure PowerShell konzolon írja be a következőt: `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="c5c64-118">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

## <span data-ttu-id="c5c64-119">Példák</span><span class="sxs-lookup"><span data-stu-id="c5c64-119">EXAMPLES</span></span>

### <span data-ttu-id="c5c64-120">1. példa: Azure-környezet hozzáadása</span><span class="sxs-lookup"><span data-stu-id="c5c64-120">Example 1: Add an Azure environment</span></span>
```
PS C:\> Add-AzureEnvironment -Name ContosoEnv -PublishSettingsFileUrl https://contoso.com/fwlink/?LinkID=101 -ServiceEndpoint https://contoso.com/fwlink/?LinkID=102

Name                          : ContosoEnv

PublishSettingsFileUrl        : https://contoso.com/fwlink/?LinkID=101

ServiceEndpoint               : https://contoso.com/fwlink/?LinkID=102

ResourceManagerEndpoint       : 

ManagementPortalUrl           : 

ActiveDirectoryEndpoint       : 

ActiveDirectoryCommonTenantId : 

StorageEndpointSuffix         : 

StorageBlobEndpointFormat     : 

StorageQueueEndpointFormat    : 

StorageTableEndpointFormat    : 

GalleryEndpoint               :
```

<span data-ttu-id="c5c64-121">Ez a parancs létrehozza a ContosoEnv Azure-környezetet.</span><span class="sxs-lookup"><span data-stu-id="c5c64-121">This command creates the ContosoEnv Azure environment.</span></span>

## <span data-ttu-id="c5c64-122">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c5c64-122">PARAMETERS</span></span>

### <span data-ttu-id="c5c64-123">-ActiveDirectoryEndpoint</span><span class="sxs-lookup"><span data-stu-id="c5c64-123">-ActiveDirectoryEndpoint</span></span>
<span data-ttu-id="c5c64-124">Az Azure Active Directory-hitelesítés végpontját adja meg az új környezetben.</span><span class="sxs-lookup"><span data-stu-id="c5c64-124">Specifies the endpoint for Azure Active Directory authentication in the new environment.</span></span>

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

### <span data-ttu-id="c5c64-125">-ActiveDirectoryServiceEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="c5c64-125">-ActiveDirectoryServiceEndpointResourceId</span></span>
<span data-ttu-id="c5c64-126">Annak a kezelési API-nek az erőforrás-AZONOSÍTÓját adja meg, amelynek az elérését az Azure Active Directory kezeli.</span><span class="sxs-lookup"><span data-stu-id="c5c64-126">Specifies the resource ID of a management API whose access is managed by Azure Active Directory.</span></span>

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

### <span data-ttu-id="c5c64-127">-AdTenant</span><span class="sxs-lookup"><span data-stu-id="c5c64-127">-AdTenant</span></span>
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

### <span data-ttu-id="c5c64-128">-AzureKeyVaultDnsSuffix</span><span class="sxs-lookup"><span data-stu-id="c5c64-128">-AzureKeyVaultDnsSuffix</span></span>
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

### <span data-ttu-id="c5c64-129">-AzureKeyVaultServiceEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="c5c64-129">-AzureKeyVaultServiceEndpointResourceId</span></span>
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

### <span data-ttu-id="c5c64-130">-EnableAdfsAuthentication</span><span class="sxs-lookup"><span data-stu-id="c5c64-130">-EnableAdfsAuthentication</span></span>
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

### <span data-ttu-id="c5c64-131">-GalleryEndpoint</span><span class="sxs-lookup"><span data-stu-id="c5c64-131">-GalleryEndpoint</span></span>
<span data-ttu-id="c5c64-132">Az Azure Resource Manager gyűjtemény azon végpontját adja meg, amely az erőforráscsoport-gyűjtemény sablonjait tárolja.</span><span class="sxs-lookup"><span data-stu-id="c5c64-132">Specifies the endpoint for the Azure Resource Manager gallery, which stores resource group gallery templates.</span></span>
<span data-ttu-id="c5c64-133">Az Azure Resource groups és a Gallery sablonjairól a Get-AzureResourceGroupGalleryTemplate című súgótémakörben talál további információt https://go.microsoft.com/fwlink/?LinkID=393052 .</span><span class="sxs-lookup"><span data-stu-id="c5c64-133">For more information about Azure resource groups and gallery templates, see the help topic for Get-AzureResourceGroupGalleryTemplatehttps://go.microsoft.com/fwlink/?LinkID=393052.</span></span>

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

### <span data-ttu-id="c5c64-134">-GraphEndpoint</span><span class="sxs-lookup"><span data-stu-id="c5c64-134">-GraphEndpoint</span></span>
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

### <span data-ttu-id="c5c64-135">-ManagementPortalUrl</span><span class="sxs-lookup"><span data-stu-id="c5c64-135">-ManagementPortalUrl</span></span>
<span data-ttu-id="c5c64-136">Az Azure felügyeleti portál URL-címét adja meg az új környezetben.</span><span class="sxs-lookup"><span data-stu-id="c5c64-136">Specifies the URL of the Azure Management Portal in the new environment.</span></span>

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

### <span data-ttu-id="c5c64-137">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="c5c64-137">-Name</span></span>
<span data-ttu-id="c5c64-138">A környezet nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="c5c64-138">Specifies a name for the environment.</span></span>
<span data-ttu-id="c5c64-139">Ehhez a paraméterhez szükség van.</span><span class="sxs-lookup"><span data-stu-id="c5c64-139">This parameter is required.</span></span>
<span data-ttu-id="c5c64-140">Ne használja az alapértelmezett környezetek, a AzureCloud és a AzureChinaCloud nevét.</span><span class="sxs-lookup"><span data-stu-id="c5c64-140">Do not use the names of the default environments, AzureCloud and AzureChinaCloud.</span></span>

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

### <span data-ttu-id="c5c64-141">-Profil</span><span class="sxs-lookup"><span data-stu-id="c5c64-141">-Profile</span></span>
<span data-ttu-id="c5c64-142">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="c5c64-142">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="c5c64-143">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="c5c64-143">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="c5c64-144">-PublishSettingsFileUrl</span><span class="sxs-lookup"><span data-stu-id="c5c64-144">-PublishSettingsFileUrl</span></span>
<span data-ttu-id="c5c64-145">A fiók közzétételi beállításainak URL-címét adja meg.</span><span class="sxs-lookup"><span data-stu-id="c5c64-145">Specifies the URL of the publish settings files for your account.</span></span>
<span data-ttu-id="c5c64-146">Az Azure közzétételi beállítások fájlja olyan XML-fájl, amely információkat tartalmaz a fiókjával és egy olyan felügyeleti tanúsítvánnyal, amely lehetővé teszi a Windows PowerShell számára az Azure-fiókjába való bejelentkezést az Ön nevében.</span><span class="sxs-lookup"><span data-stu-id="c5c64-146">An Azure publish settings file is an XML file that contains information about your account and a management certificate that allows Windows PowerShell to sign into your Azure account on your behalf.</span></span>

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

### <span data-ttu-id="c5c64-147">-ResourceManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="c5c64-147">-ResourceManagerEndpoint</span></span>
<span data-ttu-id="c5c64-148">Az Azure Resource Manager-adatok végpontját adja meg, például a fiókhoz társított erőforráscsoportok adatait.</span><span class="sxs-lookup"><span data-stu-id="c5c64-148">Specifies the endpoint for Azure Resource Manager data, including data about resource groups associated with the account.</span></span>
<span data-ttu-id="c5c64-149">Az Azure Resource Managerről az [Azure Resource Manager parancsmagok](https://go.microsoft.com/fwlink/?LinkID=394765)  ( https://go.microsoft.com/fwlink/?LinkID=394765) és a [Windows PowerShell használata az erőforrás-kezelővel](https://go.microsoft.com/fwlink/?LinkID=394767)  című témakörben olvashat bővebben https://go.microsoft.com/fwlink/?LinkID=394767) .</span><span class="sxs-lookup"><span data-stu-id="c5c64-149">For more information about Azure Resource Manager, see [Azure Resource Manager Cmdlets](https://go.microsoft.com/fwlink/?LinkID=394765)  (https://go.microsoft.com/fwlink/?LinkID=394765) and [Using Windows PowerShell with Resource Manager](https://go.microsoft.com/fwlink/?LinkID=394767)  (https://go.microsoft.com/fwlink/?LinkID=394767).</span></span>

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

### <span data-ttu-id="c5c64-150">-ServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="c5c64-150">-ServiceEndpoint</span></span>
<span data-ttu-id="c5c64-151">Az Azure Service végpont URL-címét adja meg.</span><span class="sxs-lookup"><span data-stu-id="c5c64-151">Specifies the URL of the Azure service endpoint.</span></span>
<span data-ttu-id="c5c64-152">Az Azure szolgáltatás végpontja azt határozza meg, hogy az alkalmazást a 21Vianet által Kínában üzemeltetett globális Azure platform, illetve egy privát Azure-példány kezeli-e.</span><span class="sxs-lookup"><span data-stu-id="c5c64-152">The Azure service endpoint determines whether your application is managed by the global Azure platform, Azure operated by 21Vianet in China, or a private Azure installation.</span></span>

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

### <span data-ttu-id="c5c64-153">-SqlDatabaseDnsSuffix</span><span class="sxs-lookup"><span data-stu-id="c5c64-153">-SqlDatabaseDnsSuffix</span></span>
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

### <span data-ttu-id="c5c64-154">-StorageEndpoint</span><span class="sxs-lookup"><span data-stu-id="c5c64-154">-StorageEndpoint</span></span>
<span data-ttu-id="c5c64-155">A tárolási szolgáltatások alapértelmezett végpontját adja meg az új környezetben.</span><span class="sxs-lookup"><span data-stu-id="c5c64-155">Specifies the default endpoint of storage services in the new environment.</span></span>

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

### <span data-ttu-id="c5c64-156">-TrafficManagerDnsSuffix</span><span class="sxs-lookup"><span data-stu-id="c5c64-156">-TrafficManagerDnsSuffix</span></span>
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

### <span data-ttu-id="c5c64-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c5c64-157">CommonParameters</span></span>
<span data-ttu-id="c5c64-158">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c5c64-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c5c64-159">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c5c64-159">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c5c64-160">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c5c64-160">INPUTS</span></span>

### <span data-ttu-id="c5c64-161">Nincs</span><span class="sxs-lookup"><span data-stu-id="c5c64-161">None</span></span>
<span data-ttu-id="c5c64-162">A parancsmagot tulajdonság nevében, de nem érték szerint is beírhatja.</span><span class="sxs-lookup"><span data-stu-id="c5c64-162">You can pipe input to this cmdlet by property name, but not by value.</span></span>

## <span data-ttu-id="c5c64-163">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c5c64-163">OUTPUTS</span></span>

### <span data-ttu-id="c5c64-164">Microsoft. WindowsAzure. commands. Utilities. Common. WindowsAzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="c5c64-164">Microsoft.WindowsAzure.Commands.Utilities.Common.WindowsAzureEnvironment</span></span>

## <span data-ttu-id="c5c64-165">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c5c64-165">NOTES</span></span>

## <span data-ttu-id="c5c64-166">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c5c64-166">RELATED LINKS</span></span>

[<span data-ttu-id="c5c64-167">Get-AzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="c5c64-167">Get-AzureEnvironment</span></span>](./Get-AzureEnvironment.md)

[<span data-ttu-id="c5c64-168">Remove-AzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="c5c64-168">Remove-AzureEnvironment</span></span>](./Remove-AzureEnvironment.md)

[<span data-ttu-id="c5c64-169">Set-AzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="c5c64-169">Set-AzureEnvironment</span></span>](./Set-AzureEnvironment.md)


