---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkservicetag
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkServiceTag.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkServiceTag.md
ms.openlocfilehash: c511dc6eba981708557797dc657e4626621f9131
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94195568"
---
# <span data-ttu-id="1d77a-101">Get-AzNetworkServiceTag</span><span class="sxs-lookup"><span data-stu-id="1d77a-101">Get-AzNetworkServiceTag</span></span>

## <span data-ttu-id="1d77a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="1d77a-102">SYNOPSIS</span></span>
<span data-ttu-id="1d77a-103">A szolgáltatás címke információs erőforrásainak listáját kapja meg.</span><span class="sxs-lookup"><span data-stu-id="1d77a-103">Gets the list of service tag information resources.</span></span>

## <span data-ttu-id="1d77a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="1d77a-104">SYNTAX</span></span>

```
Get-AzNetworkServiceTag -Location <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1d77a-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="1d77a-105">DESCRIPTION</span></span>
<span data-ttu-id="1d77a-106">A **Get-AzNetworkServiceTag** parancsmag a szolgáltatási címke információs erőforrásainak listáját kapja.</span><span class="sxs-lookup"><span data-stu-id="1d77a-106">The **Get-AzNetworkServiceTag** cmdlet gets the list of service tag information resources.</span></span>

<span data-ttu-id="1d77a-107">Felhívjuk a figyelmét arra, hogy a megadott Azure-régiókód a verzió hivatkozásként fog megjelenni (nem a hely szerinti szűrőként).</span><span class="sxs-lookup"><span data-stu-id="1d77a-107">Please note that the Azure region information you specify will be used as a reference for version (not as a filter based on location).</span></span> <span data-ttu-id="1d77a-108">Ha például azt adja meg, `-Location eastus2` hogy az előfizetéshez tartozó összes régióban megjelenik-e a szolgáltatás címkéi, az előfizetése (azaz nyilvános, Amerikai Egyesült Államok kormánya, Kína vagy Németország) a felhőre korlátozódik.</span><span class="sxs-lookup"><span data-stu-id="1d77a-108">For example, even if you specify `-Location eastus2` you will get the list of service tags with prefix details across all regions but limited to the cloud that your subscription belongs to (i.e. Public, US government, China or Germany).</span></span>

## <span data-ttu-id="1d77a-109">Példák</span><span class="sxs-lookup"><span data-stu-id="1d77a-109">EXAMPLES</span></span>

### <span data-ttu-id="1d77a-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="1d77a-110">Example 1</span></span>
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

<span data-ttu-id="1d77a-111">A parancs a szolgáltatás címke információs erőforrásainak listáját kapja, és a változóban tárolja `serviceTags` .</span><span class="sxs-lookup"><span data-stu-id="1d77a-111">The command gets the list of service tag information resources and stores it in variable `serviceTags`.</span></span>

### <span data-ttu-id="1d77a-112">2. példa: az összes cím előtagok beszerzése a AzureSQL-hoz</span><span class="sxs-lookup"><span data-stu-id="1d77a-112">Example 2: Get all address prefixes for AzureSQL</span></span>
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

<span data-ttu-id="1d77a-113">Az első parancs a szolgáltatás címke információs erőforrásainak listáját adja meg, és a változóban tárolja `serviceTags` .</span><span class="sxs-lookup"><span data-stu-id="1d77a-113">The first command gets the list of service tag information resources and stores it in variable `serviceTags`.</span></span>
<span data-ttu-id="1d77a-114">A második parancs a listára szűri az SQL információs erőforrását.</span><span class="sxs-lookup"><span data-stu-id="1d77a-114">The second command filters the list to select information resource for Sql.</span></span>

### <span data-ttu-id="1d77a-115">3. példa: a tárterület szolgáltatás címke információs forrása a West US 2 rendszerhez</span><span class="sxs-lookup"><span data-stu-id="1d77a-115">Example 3: Get Storage's service tag information resource for West US 2</span></span>
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

<span data-ttu-id="1d77a-116">Az első parancs a szolgáltatás címke információs erőforrásainak listáját adja meg, és a változóban tárolja `serviceTags` .</span><span class="sxs-lookup"><span data-stu-id="1d77a-116">The first command gets the list of service tag information resources and stores it in variable `serviceTags`.</span></span>
<span data-ttu-id="1d77a-117">Az alábbi parancsok azt mutatják be, hogy hogyan szűrheti a listát, ha kijelöli a szolgáltatás címke adatait a West US 2 tárterületén.</span><span class="sxs-lookup"><span data-stu-id="1d77a-117">The following commands show various way to filter the list to select service tag information for Storage in West US 2.</span></span>

### <span data-ttu-id="1d77a-118">4. példa: a globális szolgáltatási címke információs erőforrásainak beolvasása</span><span class="sxs-lookup"><span data-stu-id="1d77a-118">Example 4: Get all global service tag information resources</span></span>
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

<span data-ttu-id="1d77a-119">Az első parancs a szolgáltatás címke információs erőforrásainak listáját adja meg, és a változóban tárolja `serviceTags` .</span><span class="sxs-lookup"><span data-stu-id="1d77a-119">The first command gets the list of service tag information resources and stores it in variable `serviceTags`.</span></span>
<span data-ttu-id="1d77a-120">A második parancs szűri a listát úgy, hogy csak a régió beállítása nélkül legyen kiválasztva.</span><span class="sxs-lookup"><span data-stu-id="1d77a-120">The second command filters the list to select only those without set region.</span></span>

## <span data-ttu-id="1d77a-121">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="1d77a-121">PARAMETERS</span></span>

### <span data-ttu-id="1d77a-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1d77a-122">-DefaultProfile</span></span>
<span data-ttu-id="1d77a-123">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="1d77a-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1d77a-124">-Hely</span><span class="sxs-lookup"><span data-stu-id="1d77a-124">-Location</span></span>
<span data-ttu-id="1d77a-125">Annak a helynek a listája, amelyet a verzió hivatkozásként szeretne használni (nem szűrőn alapuló szűrőként), a szolgáltatás címkéit a minden régióban, az előfizetése által érintett felhőre korlátozva kapja meg.</span><span class="sxs-lookup"><span data-stu-id="1d77a-125">The location that will be used as a reference for version (not as a filter based on location, you will get the list of service tags with prefix details across all regions but limited to the cloud that your subscription belongs to).</span></span>

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

### <span data-ttu-id="1d77a-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1d77a-126">CommonParameters</span></span>
<span data-ttu-id="1d77a-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="1d77a-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1d77a-128">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="1d77a-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1d77a-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="1d77a-129">INPUTS</span></span>

### <span data-ttu-id="1d77a-130">System. String</span><span class="sxs-lookup"><span data-stu-id="1d77a-130">System.String</span></span>

## <span data-ttu-id="1d77a-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1d77a-131">OUTPUTS</span></span>

### <span data-ttu-id="1d77a-132">Microsoft. Azure. commands. Network. models. PSNetworkServiceTag</span><span class="sxs-lookup"><span data-stu-id="1d77a-132">Microsoft.Azure.Commands.Network.Models.PSNetworkServiceTag</span></span>

## <span data-ttu-id="1d77a-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="1d77a-133">NOTES</span></span>

## <span data-ttu-id="1d77a-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1d77a-134">RELATED LINKS</span></span>
