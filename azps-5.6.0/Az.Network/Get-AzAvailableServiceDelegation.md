---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azavailableservicedelegation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzAvailableServiceDelegation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzAvailableServiceDelegation.md
ms.openlocfilehash: d98b9d2395c0795c37fd9d7cf31dc354bde3b7cc
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101940217"
---
# <span data-ttu-id="af21f-101">Get-AzAvailableServiceDelegation</span><span class="sxs-lookup"><span data-stu-id="af21f-101">Get-AzAvailableServiceDelegation</span></span>

## <span data-ttu-id="af21f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="af21f-102">SYNOPSIS</span></span>
<span data-ttu-id="af21f-103">Elérhető szolgáltatásdelegálások a régióban.</span><span class="sxs-lookup"><span data-stu-id="af21f-103">Get available service delegations in the region.</span></span>

## <span data-ttu-id="af21f-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="af21f-104">SYNTAX</span></span>

```
Get-AzAvailableServiceDelegation -Location <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="af21f-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="af21f-105">DESCRIPTION</span></span>
<span data-ttu-id="af21f-106">A **Get-AzAvailableServiceDelegation** parancsmag lehetővé teszi az alhálózat összes rendelkezésre álló szolgáltatásdelegálásának beolvasását a megadott helyen.</span><span class="sxs-lookup"><span data-stu-id="af21f-106">The **Get-AzAvailableServiceDelegation** cmdlet allows you to retrieve all of the available service delegations for a subnet in the provided location.</span></span> <span data-ttu-id="af21f-107">Ez a parancsmag *nem* írja le, hogy mely delegáltak lehetnek együtt egyetlen alhálózaton.</span><span class="sxs-lookup"><span data-stu-id="af21f-107">This cmdlet does *not* describe which delegations may co-exist on a single subnet.</span></span>

## <span data-ttu-id="af21f-108">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="af21f-108">EXAMPLES</span></span>

### <span data-ttu-id="af21f-109">1: Az összes rendelkezésre álló szolgáltatásdelegálás lekérhetők</span><span class="sxs-lookup"><span data-stu-id="af21f-109">1: Getting all available service delegations</span></span>
```powershell
PS C:\> Get-AzAvailableServiceDelegation -Location "westus"

Name        : Microsoft.Web.serverFarms
Id          : /subscriptions/subId/providers/Microsoft.Network/availableDelegations/Microsoft.Web.serverFarms
Type        : Microsoft.Network/availableDelegations
ServiceName : Microsoft.Web/serverFarms
Actions     : {Microsoft.Network/virtualNetworks/subnets/action}

Name        : Microsoft.Sql.servers
Id          : /subscriptions/subId/providers/Microsoft.Network/availableDelegations/Microsoft.Sql.servers
Type        : Microsoft.Network/availableDelegations
ServiceName : Microsoft.Sql/servers
Actions     : {}
```

## <span data-ttu-id="af21f-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="af21f-110">PARAMETERS</span></span>

### <span data-ttu-id="af21f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="af21f-111">-DefaultProfile</span></span>
<span data-ttu-id="af21f-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="af21f-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="af21f-113">-Location</span><span class="sxs-lookup"><span data-stu-id="af21f-113">-Location</span></span>
<span data-ttu-id="af21f-114">A hely.</span><span class="sxs-lookup"><span data-stu-id="af21f-114">The location.</span></span>

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

### <span data-ttu-id="af21f-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="af21f-115">CommonParameters</span></span>
<span data-ttu-id="af21f-116">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="af21f-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="af21f-117">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="af21f-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="af21f-118">INPUTS</span><span class="sxs-lookup"><span data-stu-id="af21f-118">INPUTS</span></span>

### <span data-ttu-id="af21f-119">System.String</span><span class="sxs-lookup"><span data-stu-id="af21f-119">System.String</span></span>

## <span data-ttu-id="af21f-120">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="af21f-120">OUTPUTS</span></span>

### <span data-ttu-id="af21f-121">Microsoft.Azure.Commands.Network.Models.PSAvailableDelegation</span><span class="sxs-lookup"><span data-stu-id="af21f-121">Microsoft.Azure.Commands.Network.Models.PSAvailableDelegation</span></span>

## <span data-ttu-id="af21f-122">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="af21f-122">NOTES</span></span>

## <span data-ttu-id="af21f-123">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="af21f-123">RELATED LINKS</span></span>

<span data-ttu-id="af21f-124">[Add-AzDelegation](./Add-AzDelegation.md) 
 [New-AzDelegation](./New-AzDelegation.md) 
 [Remove-AzDelegation](./Remove-AzDelegation.md) 
 [Get-AzDelegation](./Get-AzDelegation.md)</span><span class="sxs-lookup"><span data-stu-id="af21f-124">[Add-AzDelegation](./Add-AzDelegation.md)
[New-AzDelegation](./New-AzDelegation.md)
[Remove-AzDelegation](./Remove-AzDelegation.md)
[Get-AzDelegation](./Get-AzDelegation.md)</span></span>