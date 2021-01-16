---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkservicetag
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkServiceTag.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkServiceTag.md
ms.openlocfilehash: c511dc6eba981708557797dc657e4626621f9131
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98379957"
---
# <span data-ttu-id="4dc16-101">Get-AzNetworkServiceTag</span><span class="sxs-lookup"><span data-stu-id="4dc16-101">Get-AzNetworkServiceTag</span></span>

## <span data-ttu-id="4dc16-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4dc16-102">SYNOPSIS</span></span>
<span data-ttu-id="4dc16-103">A szolgáltatáscímke-információs erőforrások listájának lekérte.</span><span class="sxs-lookup"><span data-stu-id="4dc16-103">Gets the list of service tag information resources.</span></span>

## <span data-ttu-id="4dc16-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="4dc16-104">SYNTAX</span></span>

```
Get-AzNetworkServiceTag -Location <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4dc16-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="4dc16-105">DESCRIPTION</span></span>
<span data-ttu-id="4dc16-106">A **Get-AzNetworkServiceTag parancsmag** lekérte a szolgáltatáscímke-információs erőforrások listáját.</span><span class="sxs-lookup"><span data-stu-id="4dc16-106">The **Get-AzNetworkServiceTag** cmdlet gets the list of service tag information resources.</span></span>

<span data-ttu-id="4dc16-107">Felhívjuk a figyelmét arra, hogy az Ön által megadott Azure-régióadatokat hivatkozásként fogja használni a verzióhoz (nem helyalapú szűrőként).</span><span class="sxs-lookup"><span data-stu-id="4dc16-107">Please note that the Azure region information you specify will be used as a reference for version (not as a filter based on location).</span></span> <span data-ttu-id="4dc16-108">Ha például megadja, akkor is meg fogja kapni az előtaggal kapcsolatos adatokat tartalmazó szolgáltatáscímkéket az összes régióban, de csak arra a felhőre korlátozódik, amelyhez az előfizetés tartozik (például nyilvános, egyesült államokbeli kormányzati, kínai vagy `-Location eastus2` németországi).</span><span class="sxs-lookup"><span data-stu-id="4dc16-108">For example, even if you specify `-Location eastus2` you will get the list of service tags with prefix details across all regions but limited to the cloud that your subscription belongs to (i.e. Public, US government, China or Germany).</span></span>

## <span data-ttu-id="4dc16-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="4dc16-109">EXAMPLES</span></span>

### <span data-ttu-id="4dc16-110">1. példa</span><span class="sxs-lookup"><span data-stu-id="4dc16-110">Example 1</span></span>
```powershell
PS C:\> $serviceTags = Get-AzNetworkServiceTag -Location eastus2
PS C:\> $serviceTags

Name         : Public
Id           : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxx/providers/Microsoft.Network/serviceTags/Public
Type         : Microsoft.Network/serviceTags
ChangeNumber : 63
Cloud        : Public
Values       : {ApiManagement, ApiManagement.AustraliaCentral, ApiManagement.AustraliaCentral2, ApiManagement.AustraliaEast...}

PS C:\> $serviceTags.Values

Name             : ApiManagement
System Service   : AzureApiManagement
Address Prefixes : {13.64.39.16/32, 13.66.138.92/31, 13.66.140.176/28, 13.67.8.108/31...}
Change Number    : 7

Name             : ApiManagement.AustraliaCentral
System Service   : AzureApiManagement
Region           : australiacentral
Address Prefixes : {20.36.106.68/31, 20.36.107.176/28}
Change Number    : 2

Name             : ApiManagement.AustraliaCentral2
System Service   : AzureApiManagement
Region           : australiacentral2
Address Prefixes : {20.36.114.20/31, 20.36.115.128/28}
Change Number    : 2

Name             : ApiManagement.AustraliaEast
System Service   : AzureApiManagement
Region           : australiaeast
Address Prefixes : {13.70.72.28/31, 13.70.72.240/28, 13.75.217.184/32, 13.75.221.78/32...}
Change Number    : 3

Name             : ApiManagement.AustraliaSoutheast
System Service   : AzureApiManagement
Region           : australiasoutheast
Address Prefixes : {13.77.50.68/31, 13.77.52.224/28}
Change Number    : 2

...
```

<span data-ttu-id="4dc16-111">A parancs beszerzi a szolgáltatáscímke-információforrások listáját, és változóban tárolja `serviceTags` azt.</span><span class="sxs-lookup"><span data-stu-id="4dc16-111">The command gets the list of service tag information resources and stores it in variable `serviceTags`.</span></span>

### <span data-ttu-id="4dc16-112">2. példa: Az AzureSQL összes címelőtagja</span><span class="sxs-lookup"><span data-stu-id="4dc16-112">Example 2: Get all address prefixes for AzureSQL</span></span>
```powershell
PS C:\> $serviceTags = Get-AzNetworkServiceTag -Location eastus2
PS C:\> $sql = $serviceTags.Values | Where-Object { $_.Name -eq "Sql" }
PS C:\> $sql

Name             : Sql
System Service   : AzureSQL
Address Prefixes : {13.65.31.249/32, 13.65.39.207/32, 13.65.85.183/32, 13.65.200.105/32...}
Change Number    : 18

PS C:\> $sql.Properties.AddressPrefixes.Count
644
PS C:\> $sql.Properties.AddressPrefixes
13.65.31.249/32
13.65.39.207/32
13.65.85.183/32
13.65.200.105/32
13.65.209.243/32
...
```

<span data-ttu-id="4dc16-113">Az első parancs beszerzi a szolgáltatáscímke-információforrások listáját, és változóban tárolja `serviceTags` azt.</span><span class="sxs-lookup"><span data-stu-id="4dc16-113">The first command gets the list of service tag information resources and stores it in variable `serviceTags`.</span></span>
<span data-ttu-id="4dc16-114">A második parancs szűri a listát az Sql információs erőforrásának kiválasztásához.</span><span class="sxs-lookup"><span data-stu-id="4dc16-114">The second command filters the list to select information resource for Sql.</span></span>

### <span data-ttu-id="4dc16-115">3. példa: A Tárterület szolgáltatáscímke-információs erőforrásának lekérte a Nyugat-USA 2-re</span><span class="sxs-lookup"><span data-stu-id="4dc16-115">Example 3: Get Storage's service tag information resource for West US 2</span></span>
```powershell
PS C:\> $serviceTags = Get-AzNetworkServiceTag -Location eastus2
PS C:\> $serviceTags.Values | Where-Object { $_.Name -eq "Storage.WestUS2" }

Name             : Storage.WestUS2
System Service   : AzureStorage
Region           : westus2
Address Prefixes : {13.66.176.16/28, 13.66.176.48/28, 13.66.232.64/28, 13.66.232.208/28...}
Change Number    : 5

PS C:\> $serviceTags.Values | Where-Object { $_.Name -like "Storage*" -and $_.Properties.Region -eq "westus2" }

Name             : Storage.WestUS2
System Service   : AzureStorage
Region           : westus2
Address Prefixes : {13.66.176.16/28, 13.66.176.48/28, 13.66.232.64/28, 13.66.232.208/28...}
Change Number    : 5

PS C:\> $serviceTags.Values | Where-Object { $_.Properties.SystemService -eq "AzureStorage" -and $_.Properties.Region -eq "westus2" }

Name             : Storage.WestUS2
System Service   : AzureStorage
Region           : westus2
Address Prefixes : {13.66.176.16/28, 13.66.176.48/28, 13.66.232.64/28, 13.66.232.208/28...}
Change Number    : 5
```

<span data-ttu-id="4dc16-116">Az első parancs beszerzi a szolgáltatáscímke-információforrások listáját, és változóban tárolja `serviceTags` azt.</span><span class="sxs-lookup"><span data-stu-id="4dc16-116">The first command gets the list of service tag information resources and stores it in variable `serviceTags`.</span></span>
<span data-ttu-id="4dc16-117">Az alábbi parancsok a lista szűrésének különféle módjait mutatják be a 2. nyugat-amerikai 2. tárhely szolgáltatáscímke-információinak kiválasztásához.</span><span class="sxs-lookup"><span data-stu-id="4dc16-117">The following commands show various way to filter the list to select service tag information for Storage in West US 2.</span></span>

### <span data-ttu-id="4dc16-118">4. példa: Az összes globális szolgáltatáscímke-információforrás lekérte</span><span class="sxs-lookup"><span data-stu-id="4dc16-118">Example 4: Get all global service tag information resources</span></span>
```powershell
PS C:\> $serviceTags = Get-AzNetworkServiceTag -Location eastus2
PS C:\> $serviceTags.Values | Where-Object { -not $_.Properties.Region }


Name             : ApiManagement
System Service   : AzureApiManagement
Address Prefixes : {13.64.39.16/32, 13.66.138.92/31, 13.66.140.176/28, 13.67.8.108/31...}
Change Number    : 7

Name             : AppService
System Service   : AzureAppService
Address Prefixes : {13.64.73.110/32, 13.65.30.245/32, 13.65.37.122/32, 13.65.39.165/32...}
Change Number    : 13

Name             : AppServiceManagement
System Service   : AzureAppServiceManagement
Address Prefixes : {13.64.115.203/32, 13.66.140.0/26, 13.67.8.128/26, 13.69.64.128/26...}
Change Number    : 7

Name             : AzureActiveDirectory
System Service   : AzureAD
Address Prefixes : {13.64.151.161/32, 13.66.141.64/27, 13.67.9.224/27, 13.67.50.224/29...}
Change Number    : 3

Name             : AzureActiveDirectoryDomainServices
System Service   : AzureIdentity
Address Prefixes : {13.64.151.161/32, 13.66.141.64/27, 13.67.9.224/27, 13.69.66.160/27...}
Change Number    : 2

...
```

<span data-ttu-id="4dc16-119">Az első parancs beszerzi a szolgáltatáscímke-információforrások listáját, és változóban tárolja `serviceTags` azt.</span><span class="sxs-lookup"><span data-stu-id="4dc16-119">The first command gets the list of service tag information resources and stores it in variable `serviceTags`.</span></span>
<span data-ttu-id="4dc16-120">A második parancs szűri a listát, hogy csak a beállított terület nélkülieket jelölje ki.</span><span class="sxs-lookup"><span data-stu-id="4dc16-120">The second command filters the list to select only those without set region.</span></span>

## <span data-ttu-id="4dc16-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4dc16-121">PARAMETERS</span></span>

### <span data-ttu-id="4dc16-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4dc16-122">-DefaultProfile</span></span>
<span data-ttu-id="4dc16-123">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="4dc16-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4dc16-124">-Location</span><span class="sxs-lookup"><span data-stu-id="4dc16-124">-Location</span></span>
<span data-ttu-id="4dc16-125">A verzió hivatkozásaként használt hely (nem helyalapú szűrőként) az összes régióra vonatkozó előtagadatokat tartalmazó szolgáltatáscímkék listáját fogja kapni, de csak arra a felhőre, amelyhez az előfizetés tartozik).</span><span class="sxs-lookup"><span data-stu-id="4dc16-125">The location that will be used as a reference for version (not as a filter based on location, you will get the list of service tags with prefix details across all regions but limited to the cloud that your subscription belongs to).</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4dc16-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4dc16-126">CommonParameters</span></span>
<span data-ttu-id="4dc16-127">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4dc16-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4dc16-128">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4dc16-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4dc16-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="4dc16-129">INPUTS</span></span>

### <span data-ttu-id="4dc16-130">System.String</span><span class="sxs-lookup"><span data-stu-id="4dc16-130">System.String</span></span>

## <span data-ttu-id="4dc16-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4dc16-131">OUTPUTS</span></span>

### <span data-ttu-id="4dc16-132">Microsoft.Azure.Commands.Network.Models.PSNetworkServiceTag</span><span class="sxs-lookup"><span data-stu-id="4dc16-132">Microsoft.Azure.Commands.Network.Models.PSNetworkServiceTag</span></span>

## <span data-ttu-id="4dc16-133">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="4dc16-133">NOTES</span></span>

## <span data-ttu-id="4dc16-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4dc16-134">RELATED LINKS</span></span>
