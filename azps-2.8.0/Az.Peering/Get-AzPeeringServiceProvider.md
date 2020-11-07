---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/get-azpeeringserviceprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeeringServiceProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeeringServiceProvider.md
ms.openlocfilehash: 786a8009d1423b6b12fae4d7eb8da6899a8cd108
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93838433"
---
# <span data-ttu-id="28643-101">Get-AzPeeringServiceProvider</span><span class="sxs-lookup"><span data-stu-id="28643-101">Get-AzPeeringServiceProvider</span></span>

## <span data-ttu-id="28643-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="28643-102">SYNOPSIS</span></span>
<span data-ttu-id="28643-103">A Microsofttal együttműködő együttműködő szolgáltatók listáját kapja meg.</span><span class="sxs-lookup"><span data-stu-id="28643-103">Gets a list of peering service providers partnered with Microsoft.</span></span>

## <span data-ttu-id="28643-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="28643-104">SYNTAX</span></span>

```
Get-AzPeeringServiceProvider [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="28643-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="28643-105">DESCRIPTION</span></span>
<span data-ttu-id="28643-106">A lista-társas szolgáltatók listája</span><span class="sxs-lookup"><span data-stu-id="28643-106">List peering service providers</span></span>

## <span data-ttu-id="28643-107">Példák</span><span class="sxs-lookup"><span data-stu-id="28643-107">EXAMPLES</span></span>

### <span data-ttu-id="28643-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="28643-108">Example 1</span></span>
```powershell
PS C:\> Get-AzPeeringServiceProvider

ServiceProviderName Name      Id Type
------------------- ----      -- ----
TestPeer1           TestPeer1    Microsoft.Peering/peeringServiceProviders
```

<span data-ttu-id="28643-109">Elérhető társközi szolgáltatók</span><span class="sxs-lookup"><span data-stu-id="28643-109">Gets available peering service providers</span></span>

## <span data-ttu-id="28643-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="28643-110">PARAMETERS</span></span>

### <span data-ttu-id="28643-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="28643-111">-DefaultProfile</span></span>
<span data-ttu-id="28643-112">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="28643-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="28643-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="28643-113">CommonParameters</span></span>
<span data-ttu-id="28643-114">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="28643-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="28643-115">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="28643-115">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="28643-116">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="28643-116">INPUTS</span></span>

### <span data-ttu-id="28643-117">Nincs</span><span class="sxs-lookup"><span data-stu-id="28643-117">None</span></span>

## <span data-ttu-id="28643-118">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="28643-118">OUTPUTS</span></span>

### <span data-ttu-id="28643-119">Microsoft. Azure. PowerShell. parancsmagok. társközi. models. PSPeeringServiceProvider</span><span class="sxs-lookup"><span data-stu-id="28643-119">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringServiceProvider</span></span>

## <span data-ttu-id="28643-120">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="28643-120">NOTES</span></span>

## <span data-ttu-id="28643-121">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="28643-121">RELATED LINKS</span></span>
