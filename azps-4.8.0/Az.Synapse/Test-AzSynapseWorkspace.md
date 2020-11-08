---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/test-azsynapseworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Test-AzSynapseWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Test-AzSynapseWorkspace.md
ms.openlocfilehash: b3dd32ec177aaa38e8fbb1f66559592f84905f2d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94183456"
---
# <span data-ttu-id="36bf1-101">Test-AzSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="36bf1-101">Test-AzSynapseWorkspace</span></span>

## <span data-ttu-id="36bf1-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="36bf1-102">SYNOPSIS</span></span>
<span data-ttu-id="36bf1-103">A szinapszis Analytics-munkaterület létezésének ellenőrzése.</span><span class="sxs-lookup"><span data-stu-id="36bf1-103">Checks for the existence of a Synapse Analytics workspace.</span></span>

## <span data-ttu-id="36bf1-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="36bf1-104">SYNTAX</span></span>

```
Test-AzSynapseWorkspace [-Name] <String> [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="36bf1-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="36bf1-105">DESCRIPTION</span></span>
<span data-ttu-id="36bf1-106">A **AzSynapseWorkspace** parancsmag ellenőrzi a szinapszis Analytics-munkaterület létezését.</span><span class="sxs-lookup"><span data-stu-id="36bf1-106">The **Test-AzSynapseWorkspace** cmdlet checks for the existence of a Synapse Analytics workspace.</span></span>

## <span data-ttu-id="36bf1-107">Példák</span><span class="sxs-lookup"><span data-stu-id="36bf1-107">EXAMPLES</span></span>

### <span data-ttu-id="36bf1-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="36bf1-108">Example 1</span></span>
```powershell
PS C:\> Test-AzSynapseWorkspace -Name ContosoWorkspace
```

<span data-ttu-id="36bf1-109">Ez a parancs a szinapszis Analytics-munkaterület létezését ellenőrzi.</span><span class="sxs-lookup"><span data-stu-id="36bf1-109">This command checks for the existence of a Synapse Analytics workspace.</span></span>

## <span data-ttu-id="36bf1-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="36bf1-110">PARAMETERS</span></span>

### <span data-ttu-id="36bf1-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="36bf1-111">-DefaultProfile</span></span>
<span data-ttu-id="36bf1-112">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="36bf1-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="36bf1-113">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="36bf1-113">-Name</span></span>
<span data-ttu-id="36bf1-114">A szinapszis munkaterületének neve.</span><span class="sxs-lookup"><span data-stu-id="36bf1-114">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36bf1-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="36bf1-115">-ResourceGroupName</span></span>
<span data-ttu-id="36bf1-116">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="36bf1-116">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36bf1-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="36bf1-117">CommonParameters</span></span>
<span data-ttu-id="36bf1-118">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="36bf1-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="36bf1-119">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="36bf1-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="36bf1-120">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="36bf1-120">INPUTS</span></span>

### <span data-ttu-id="36bf1-121">Nincs</span><span class="sxs-lookup"><span data-stu-id="36bf1-121">None</span></span>

## <span data-ttu-id="36bf1-122">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="36bf1-122">OUTPUTS</span></span>

### <span data-ttu-id="36bf1-123">System. Object (rendszer. objektum)</span><span class="sxs-lookup"><span data-stu-id="36bf1-123">System.Object</span></span>
## <span data-ttu-id="36bf1-124">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="36bf1-124">NOTES</span></span>

## <span data-ttu-id="36bf1-125">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="36bf1-125">RELATED LINKS</span></span>
