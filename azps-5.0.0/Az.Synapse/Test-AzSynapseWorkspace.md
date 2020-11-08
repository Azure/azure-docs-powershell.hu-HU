---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/test-azsynapseworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Test-AzSynapseWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Test-AzSynapseWorkspace.md
ms.openlocfilehash: b3dd32ec177aaa38e8fbb1f66559592f84905f2d
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94185142"
---
# <span data-ttu-id="14235-101">Test-AzSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="14235-101">Test-AzSynapseWorkspace</span></span>

## <span data-ttu-id="14235-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="14235-102">SYNOPSIS</span></span>
<span data-ttu-id="14235-103">A szinapszis Analytics-munkaterület létezésének ellenőrzése.</span><span class="sxs-lookup"><span data-stu-id="14235-103">Checks for the existence of a Synapse Analytics workspace.</span></span>

## <span data-ttu-id="14235-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="14235-104">SYNTAX</span></span>

```
Test-AzSynapseWorkspace [-Name] <String> [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="14235-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="14235-105">DESCRIPTION</span></span>
<span data-ttu-id="14235-106">A **AzSynapseWorkspace** parancsmag ellenőrzi a szinapszis Analytics-munkaterület létezését.</span><span class="sxs-lookup"><span data-stu-id="14235-106">The **Test-AzSynapseWorkspace** cmdlet checks for the existence of a Synapse Analytics workspace.</span></span>

## <span data-ttu-id="14235-107">Példák</span><span class="sxs-lookup"><span data-stu-id="14235-107">EXAMPLES</span></span>

### <span data-ttu-id="14235-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="14235-108">Example 1</span></span>
```powershell
PS C:\> Test-AzSynapseWorkspace -Name ContosoWorkspace
```

<span data-ttu-id="14235-109">Ez a parancs a szinapszis Analytics-munkaterület létezését ellenőrzi.</span><span class="sxs-lookup"><span data-stu-id="14235-109">This command checks for the existence of a Synapse Analytics workspace.</span></span>

## <span data-ttu-id="14235-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="14235-110">PARAMETERS</span></span>

### <span data-ttu-id="14235-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="14235-111">-DefaultProfile</span></span>
<span data-ttu-id="14235-112">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="14235-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="14235-113">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="14235-113">-Name</span></span>
<span data-ttu-id="14235-114">A szinapszis munkaterületének neve.</span><span class="sxs-lookup"><span data-stu-id="14235-114">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="14235-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="14235-115">-ResourceGroupName</span></span>
<span data-ttu-id="14235-116">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="14235-116">Resource group name.</span></span>

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

### <span data-ttu-id="14235-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="14235-117">CommonParameters</span></span>
<span data-ttu-id="14235-118">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="14235-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="14235-119">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="14235-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="14235-120">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="14235-120">INPUTS</span></span>

### <span data-ttu-id="14235-121">Nincs</span><span class="sxs-lookup"><span data-stu-id="14235-121">None</span></span>

## <span data-ttu-id="14235-122">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="14235-122">OUTPUTS</span></span>

### <span data-ttu-id="14235-123">System. Object (rendszer. objektum)</span><span class="sxs-lookup"><span data-stu-id="14235-123">System.Object</span></span>
## <span data-ttu-id="14235-124">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="14235-124">NOTES</span></span>

## <span data-ttu-id="14235-125">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="14235-125">RELATED LINKS</span></span>
