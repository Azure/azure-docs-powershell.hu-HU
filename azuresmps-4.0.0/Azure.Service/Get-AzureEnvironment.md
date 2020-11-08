---
external help file: Microsoft.WindowsAzure.Commands.Profile.dll-Help.xml
ms.assetid: BF5E3E1A-14B6-4630-8168-628057009D5E
online version: ''
schema: 2.0.0
ms.openlocfilehash: 284d1601746254b2e10fdfe042e5882e94ca1bd9
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016352"
---
# <span data-ttu-id="7927f-101">Get-AzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="7927f-101">Get-AzureEnvironment</span></span>

## <span data-ttu-id="7927f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="7927f-102">SYNOPSIS</span></span>
<span data-ttu-id="7927f-103">Azure-környezetek beolvasása</span><span class="sxs-lookup"><span data-stu-id="7927f-103">Gets Azure environments</span></span>

## <span data-ttu-id="7927f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="7927f-104">SYNTAX</span></span>

```
Get-AzureEnvironment [-Name <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="7927f-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="7927f-105">DESCRIPTION</span></span>
<span data-ttu-id="7927f-106">A **Get-AzureEnvironment** parancsmag a Windows powershellhez elérhető Azure-környezetet kapja.</span><span class="sxs-lookup"><span data-stu-id="7927f-106">The **Get-AzureEnvironment** cmdlet gets the Azure environments that are available to Windows PowerShell.</span></span>

<span data-ttu-id="7927f-107">Azure-környezet: a Microsoft Azure független központi üzembe állítása, például a AzureCloud a globális Azure-és a AzureChinaCloud által üzemeltetett Azure-alapú 21Vianet Kínában.</span><span class="sxs-lookup"><span data-stu-id="7927f-107">An Azure environment an independent deployment of Microsoft Azure, such as AzureCloud for global Azure and AzureChinaCloud for Azure operated by 21Vianet in China.</span></span>
<span data-ttu-id="7927f-108">A helyszíni Azure-környezeteket az Azure Pack és a WAPack parancsmagok használatával is létrehozhatja.</span><span class="sxs-lookup"><span data-stu-id="7927f-108">You can also create on-premises Azure environments by using Azure Pack and the WAPack cmdlets.</span></span>
<span data-ttu-id="7927f-109">További tudnivalókat az [Azure Pack (csomag](https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx)  ) című témakörben talál https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx) .</span><span class="sxs-lookup"><span data-stu-id="7927f-109">For more information, see [Azure Pack](https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx)  (https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx).</span></span>

<span data-ttu-id="7927f-110">A **Get-AzureEnvironment** parancsmag nem az Azure-ról származó környezetekre, hanem az előfizetési adatfájlból kapja a környezetét.</span><span class="sxs-lookup"><span data-stu-id="7927f-110">The **Get-AzureEnvironment** cmdlet gets environments from your subscription data file, not from Azure.</span></span>
<span data-ttu-id="7927f-111">Ha az előfizetési adatfájl elavult, futtassa a **Add-AzureAccount** vagy az **import-PublishSettingsFile** parancsmagot a frissítéséhez.</span><span class="sxs-lookup"><span data-stu-id="7927f-111">If the subscription data file is outdated, run the **Add-AzureAccount** or **Import-PublishSettingsFile** cmdlet to refresh it.</span></span>

<span data-ttu-id="7927f-112">Ez a témakör a Microsoft Azure PowerShell modul 0.8.10 verziójában található parancsmagot ismerteti.</span><span class="sxs-lookup"><span data-stu-id="7927f-112">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="7927f-113">A használt modul verziójának beszerzéséhez az Azure PowerShell konzolon írja be a következőt: `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="7927f-113">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

## <span data-ttu-id="7927f-114">Példák</span><span class="sxs-lookup"><span data-stu-id="7927f-114">EXAMPLES</span></span>

### <span data-ttu-id="7927f-115">Példa 1: az összes környezet beszerzése</span><span class="sxs-lookup"><span data-stu-id="7927f-115">Example 1: Get all environments</span></span>
```
PS C:\> Get-AzureEnvironment

EnvironmentName               ServiceEndpoint               ResourceManagerEndpoint       PublishSettingsFileUrl
---------------               ---------------               -----------------------       ----------------------

AzureCloud                    https://management.core.wi... https://management.azure.com/ https://go.microsoft.com/fw... 
AzureChinaCloud               https://management.core.ch... https://not-supported-serv... https://go.microsoft.com/fw...
```

<span data-ttu-id="7927f-116">Ez a parancs a Windows PowerShellhez elérhető összes környezetet bekapja.</span><span class="sxs-lookup"><span data-stu-id="7927f-116">This command gets all environments that are available to Windows PowerShell.</span></span>

### <span data-ttu-id="7927f-117">2. példa: környezet beszerzése név alapján</span><span class="sxs-lookup"><span data-stu-id="7927f-117">Example 2: Get an environment by name</span></span>
```
PS C:\> Get-AzureEnvironment -Name AzureCloud

Name                          : AzureCloud

PublishSettingsFileUrl        : https://go.microsoft.com/fwlink/?LinkID=301775

ServiceEndpoint               : https://management.core.windows.net/

ResourceManagerEndpoint       : https://management.azure.com/

ManagementPortalUrl           : https://go.microsoft.com/fwlink/?LinkId=254433

ActiveDirectoryEndpoint       : https://login.windows.net/

ActiveDirectoryCommonTenantId : common

StorageEndpointSuffix         : core.windows.net

StorageBlobEndpointFormat     : {0}://{1}.blob.core.windows.net/

StorageQueueEndpointFormat    : {0}://{1}.queue.core.windows.net/

StorageTableEndpointFormat    : {0}://{1}.table.core.windows.net/

GalleryEndpoint               : https://gallery.azure.com/
```

<span data-ttu-id="7927f-118">Ez a példa a AzureCloud környezetet kapja.</span><span class="sxs-lookup"><span data-stu-id="7927f-118">This example gets the AzureCloud environment.</span></span>

### <span data-ttu-id="7927f-119">3. példa: a minden környezet összes tulajdonságának lekérése</span><span class="sxs-lookup"><span data-stu-id="7927f-119">Example 3: Get all properties of all environments</span></span>
```
PS C:\> Get-AzureEnvironment | ForEach-Object {Get-AzureEnvironment -Name $_.EnvironmentName}
```

<span data-ttu-id="7927f-120">Ez a parancs a környezet minden tulajdonságát beolvassa.</span><span class="sxs-lookup"><span data-stu-id="7927f-120">This command gets all properties of all environments.</span></span>

<span data-ttu-id="7927f-121">A parancs a **Get-AzureEnvironment** parancsmagot használja az Azure-környezetek ehhez a fiókhoz való beolvasásához.</span><span class="sxs-lookup"><span data-stu-id="7927f-121">The command uses the **Get-AzureEnvironment** cmdlet to get all Azure environments for this account.</span></span>
<span data-ttu-id="7927f-122">Ezután a **foreach-Object** parancsmagot használja a **Get-AzureEnvironment** parancs futtatásához az egyes környezetekben a **Name** paraméterrel.</span><span class="sxs-lookup"><span data-stu-id="7927f-122">Then, it uses the **Foreach-Object** cmdlet to run a **Get-AzureEnvironment** command with the **Name** parameter on each environment.</span></span>
<span data-ttu-id="7927f-123">A **Name** paraméter értéke az egyes környezetek **EnvironmentName** tulajdonsága.</span><span class="sxs-lookup"><span data-stu-id="7927f-123">The value of the **Name** parameter is the **EnvironmentName** property of each environment.</span></span>

<span data-ttu-id="7927f-124">Paraméterek nélkül a **Get-AzureEnvironment** csak a környezet kijelölt tulajdonságait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="7927f-124">Without parameters, **Get-AzureEnvironment** gets only selected properties of an environment.</span></span>

## <span data-ttu-id="7927f-125">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="7927f-125">PARAMETERS</span></span>

### <span data-ttu-id="7927f-126">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="7927f-126">-Name</span></span>
<span data-ttu-id="7927f-127">Csak a megadott környezetet kapja meg.</span><span class="sxs-lookup"><span data-stu-id="7927f-127">Gets only the specified environment.</span></span>
<span data-ttu-id="7927f-128">Írja be a környezet nevét.</span><span class="sxs-lookup"><span data-stu-id="7927f-128">Type the environment name.</span></span>
<span data-ttu-id="7927f-129">A paraméter értéke megkülönbözteti a kis-és nagybetűket.</span><span class="sxs-lookup"><span data-stu-id="7927f-129">The parameter value is case-sensitive.</span></span>
<span data-ttu-id="7927f-130">A helyettesítő karakterek nem engedélyezettek.</span><span class="sxs-lookup"><span data-stu-id="7927f-130">Wildcard characters are not permitted.</span></span>

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

### <span data-ttu-id="7927f-131">-Profil</span><span class="sxs-lookup"><span data-stu-id="7927f-131">-Profile</span></span>
<span data-ttu-id="7927f-132">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="7927f-132">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="7927f-133">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="7927f-133">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="7927f-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7927f-134">CommonParameters</span></span>
<span data-ttu-id="7927f-135">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="7927f-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7927f-136">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7927f-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7927f-137">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="7927f-137">INPUTS</span></span>

### <span data-ttu-id="7927f-138">Nincs</span><span class="sxs-lookup"><span data-stu-id="7927f-138">None</span></span>
<span data-ttu-id="7927f-139">A parancsmagot tulajdonság nevében, de nem érték szerint is beírhatja.</span><span class="sxs-lookup"><span data-stu-id="7927f-139">You can pipe input to this cmdlet by property name, but not by value.</span></span>

## <span data-ttu-id="7927f-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7927f-140">OUTPUTS</span></span>

### <span data-ttu-id="7927f-141">System. Management. Automation. PSCustomObject</span><span class="sxs-lookup"><span data-stu-id="7927f-141">System.Management.Automation.PSCustomObject</span></span>
<span data-ttu-id="7927f-142">Alapértelmezés szerint a **Get-AzureEnvironment** egy egyéni objektumot ad eredményül.</span><span class="sxs-lookup"><span data-stu-id="7927f-142">By default, **Get-AzureEnvironment** returns a custom object.</span></span>

### <span data-ttu-id="7927f-143">Microsoft. WindowsAzure. commands. Utilities. Common. WindowsAzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="7927f-143">Microsoft.WindowsAzure.Commands.Utilities.Common.WindowsAzureEnvironment</span></span>
<span data-ttu-id="7927f-144">Amikor a **Get-AzureEnvironment** a **Name** paraméterrel futtatja, a  **WindowsAzureEnvironment** -objektumot adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="7927f-144">When you run **Get-AzureEnvironment** with the **Name** parameter, it returns a  **WindowsAzureEnvironment** object.</span></span>

## <span data-ttu-id="7927f-145">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="7927f-145">NOTES</span></span>

## <span data-ttu-id="7927f-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7927f-146">RELATED LINKS</span></span>

[<span data-ttu-id="7927f-147">Add-AzureAccount</span><span class="sxs-lookup"><span data-stu-id="7927f-147">Add-AzureAccount</span></span>](./Add-AzureAccount.md)

[<span data-ttu-id="7927f-148">Add-AzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="7927f-148">Add-AzureEnvironment</span></span>](./Add-AzureEnvironment.md)

[<span data-ttu-id="7927f-149">Get-AzurePublishSettingsFile</span><span class="sxs-lookup"><span data-stu-id="7927f-149">Get-AzurePublishSettingsFile</span></span>](./Get-AzurePublishSettingsFile.md)

[<span data-ttu-id="7927f-150">Importálás – AzurePublishSettingsFile</span><span class="sxs-lookup"><span data-stu-id="7927f-150">Import-AzurePublishSettingsFile</span></span>](./Import-AzurePublishSettingsFile.md)

[<span data-ttu-id="7927f-151">Remove-AzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="7927f-151">Remove-AzureEnvironment</span></span>](./Remove-AzureEnvironment.md)

[<span data-ttu-id="7927f-152">Set-AzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="7927f-152">Set-AzureEnvironment</span></span>](./Set-AzureEnvironment.md)


