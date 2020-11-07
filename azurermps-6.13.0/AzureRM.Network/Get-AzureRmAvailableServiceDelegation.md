---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermavailableservicedelegation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmAvailableServiceDelegation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmAvailableServiceDelegation.md
ms.openlocfilehash: bc5c09913209713df192603aff7ea7646e651699
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93679154"
---
# <span data-ttu-id="e4b60-101">Get-AzureRmAvailableServiceDelegation</span><span class="sxs-lookup"><span data-stu-id="e4b60-101">Get-AzureRmAvailableServiceDelegation</span></span>

## <span data-ttu-id="e4b60-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e4b60-102">SYNOPSIS</span></span>
<span data-ttu-id="e4b60-103">Elérhető szolgáltatási delegációk beszerzése a régióban.</span><span class="sxs-lookup"><span data-stu-id="e4b60-103">Get available service delegations in the region.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e4b60-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e4b60-104">SYNTAX</span></span>

```
Get-AzureRmAvailableServiceDelegation -Location <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e4b60-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="e4b60-105">DESCRIPTION</span></span>
<span data-ttu-id="e4b60-106">A **Get-AzureRmAvailableServiceDelegation** parancsmag lehetővé teszi, hogy az összes elérhető szolgáltatás-delegálást visszanyerje egy alhálózatra a megadott helyen.</span><span class="sxs-lookup"><span data-stu-id="e4b60-106">The **Get-AzureRmAvailableServiceDelegation** cmdlet allows you to retrieve all of the available service delegations for a subnet in the provided location.</span></span> <span data-ttu-id="e4b60-107">Ez a parancsmag *nem* ismerteti, hogy mely delegált lehet egyetlen alhálózaton együtt.</span><span class="sxs-lookup"><span data-stu-id="e4b60-107">This cmdlet does *not* describe which delegations may co-exist on a single subnet.</span></span>

## <span data-ttu-id="e4b60-108">Példák</span><span class="sxs-lookup"><span data-stu-id="e4b60-108">EXAMPLES</span></span>

### <span data-ttu-id="e4b60-109">1: az összes elérhető szolgáltatás-meghatalmazás beszerzése</span><span class="sxs-lookup"><span data-stu-id="e4b60-109">1: Getting all available service delegations</span></span>
```powershell
PS C:\> Get-AzureRmAvailableServiceDelegation -Location "westus"

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

## <span data-ttu-id="e4b60-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e4b60-110">PARAMETERS</span></span>

### <span data-ttu-id="e4b60-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e4b60-111">-DefaultProfile</span></span>
<span data-ttu-id="e4b60-112">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e4b60-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4b60-113">-Hely</span><span class="sxs-lookup"><span data-stu-id="e4b60-113">-Location</span></span>
<span data-ttu-id="e4b60-114">A hely.</span><span class="sxs-lookup"><span data-stu-id="e4b60-114">The location.</span></span>

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

### <span data-ttu-id="e4b60-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e4b60-115">CommonParameters</span></span>
<span data-ttu-id="e4b60-116">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e4b60-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="e4b60-117">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e4b60-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e4b60-118">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e4b60-118">INPUTS</span></span>

### <span data-ttu-id="e4b60-119">System. String</span><span class="sxs-lookup"><span data-stu-id="e4b60-119">System.String</span></span>

## <span data-ttu-id="e4b60-120">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e4b60-120">OUTPUTS</span></span>

### <span data-ttu-id="e4b60-121">Microsoft. Azure. commands. Network. models. PSAvailableDelegation</span><span class="sxs-lookup"><span data-stu-id="e4b60-121">Microsoft.Azure.Commands.Network.Models.PSAvailableDelegation</span></span>

## <span data-ttu-id="e4b60-122">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e4b60-122">NOTES</span></span>

## <span data-ttu-id="e4b60-123">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e4b60-123">RELATED LINKS</span></span>
<span data-ttu-id="e4b60-124">[Add-AzureRmDelegation](./Add-AzureRmDelegation.md) 
 [Új – AzureRmDelegation](./New-AzureRmDelegation.md) 
 [Remove-AzureRmDelegation](./Remove-AzureRmDelegation.md) 
 [Get-AzureRmDelegation](./Get-AzureRmDelegation.md)</span><span class="sxs-lookup"><span data-stu-id="e4b60-124">[Add-AzureRmDelegation](./Add-AzureRmDelegation.md)
[New-AzureRmDelegation](./New-AzureRmDelegation.md)
[Remove-AzureRmDelegation](./Remove-AzureRmDelegation.md)
[Get-AzureRmDelegation](./Get-AzureRmDelegation.md)</span></span>
