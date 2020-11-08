---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azavailableservicedelegation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzAvailableServiceDelegation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzAvailableServiceDelegation.md
ms.openlocfilehash: 169b7c2daffdf2c241a60468e745752ac7582d7d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94181113"
---
# <span data-ttu-id="b45c3-101">Get-AzAvailableServiceDelegation</span><span class="sxs-lookup"><span data-stu-id="b45c3-101">Get-AzAvailableServiceDelegation</span></span>

## <span data-ttu-id="b45c3-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b45c3-102">SYNOPSIS</span></span>
<span data-ttu-id="b45c3-103">Elérhető szolgáltatási delegációk beszerzése a régióban.</span><span class="sxs-lookup"><span data-stu-id="b45c3-103">Get available service delegations in the region.</span></span>

## <span data-ttu-id="b45c3-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b45c3-104">SYNTAX</span></span>

```
Get-AzAvailableServiceDelegation -Location <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b45c3-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="b45c3-105">DESCRIPTION</span></span>
<span data-ttu-id="b45c3-106">A **Get-AzAvailableServiceDelegation** parancsmag lehetővé teszi, hogy az összes elérhető szolgáltatás-delegálást visszanyerje egy alhálózatra a megadott helyen.</span><span class="sxs-lookup"><span data-stu-id="b45c3-106">The **Get-AzAvailableServiceDelegation** cmdlet allows you to retrieve all of the available service delegations for a subnet in the provided location.</span></span> <span data-ttu-id="b45c3-107">Ez a parancsmag *nem* ismerteti, hogy mely delegált lehet egyetlen alhálózaton együtt.</span><span class="sxs-lookup"><span data-stu-id="b45c3-107">This cmdlet does *not* describe which delegations may co-exist on a single subnet.</span></span>

## <span data-ttu-id="b45c3-108">Példák</span><span class="sxs-lookup"><span data-stu-id="b45c3-108">EXAMPLES</span></span>

### <span data-ttu-id="b45c3-109">1: az összes elérhető szolgáltatás-meghatalmazás beszerzése</span><span class="sxs-lookup"><span data-stu-id="b45c3-109">1: Getting all available service delegations</span></span>
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

## <span data-ttu-id="b45c3-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b45c3-110">PARAMETERS</span></span>

### <span data-ttu-id="b45c3-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b45c3-111">-DefaultProfile</span></span>
<span data-ttu-id="b45c3-112">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b45c3-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b45c3-113">-Hely</span><span class="sxs-lookup"><span data-stu-id="b45c3-113">-Location</span></span>
<span data-ttu-id="b45c3-114">A hely.</span><span class="sxs-lookup"><span data-stu-id="b45c3-114">The location.</span></span>

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

### <span data-ttu-id="b45c3-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b45c3-115">CommonParameters</span></span>
<span data-ttu-id="b45c3-116">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b45c3-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b45c3-117">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="b45c3-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b45c3-118">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b45c3-118">INPUTS</span></span>

### <span data-ttu-id="b45c3-119">System. String</span><span class="sxs-lookup"><span data-stu-id="b45c3-119">System.String</span></span>

## <span data-ttu-id="b45c3-120">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b45c3-120">OUTPUTS</span></span>

### <span data-ttu-id="b45c3-121">Microsoft. Azure. commands. Network. models. PSAvailableDelegation</span><span class="sxs-lookup"><span data-stu-id="b45c3-121">Microsoft.Azure.Commands.Network.Models.PSAvailableDelegation</span></span>

## <span data-ttu-id="b45c3-122">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b45c3-122">NOTES</span></span>

## <span data-ttu-id="b45c3-123">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b45c3-123">RELATED LINKS</span></span>

<span data-ttu-id="b45c3-124">[Add-AzDelegation](./Add-AzDelegation.md) 
 [Új – AzDelegation](./New-AzDelegation.md) 
 [Remove-AzDelegation](./Remove-AzDelegation.md) 
 [Get-AzDelegation](./Get-AzDelegation.md)</span><span class="sxs-lookup"><span data-stu-id="b45c3-124">[Add-AzDelegation](./Add-AzDelegation.md)
[New-AzDelegation](./New-AzDelegation.md)
[Remove-AzDelegation](./Remove-AzDelegation.md)
[Get-AzDelegation](./Get-AzDelegation.md)</span></span>