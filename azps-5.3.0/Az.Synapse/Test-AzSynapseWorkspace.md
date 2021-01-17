---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/test-azsynapseworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Test-AzSynapseWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Test-AzSynapseWorkspace.md
ms.openlocfilehash: b3dd32ec177aaa38e8fbb1f66559592f84905f2d
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98469253"
---
# <span data-ttu-id="4f1f2-101">Test-AzSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="4f1f2-101">Test-AzSynapseWorkspace</span></span>

## <span data-ttu-id="4f1f2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4f1f2-102">SYNOPSIS</span></span>
<span data-ttu-id="4f1f2-103">Ellenőrzi, hogy létezik-e Synapse Analytics-munkaterület.</span><span class="sxs-lookup"><span data-stu-id="4f1f2-103">Checks for the existence of a Synapse Analytics workspace.</span></span>

## <span data-ttu-id="4f1f2-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="4f1f2-104">SYNTAX</span></span>

```
Test-AzSynapseWorkspace [-Name] <String> [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4f1f2-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="4f1f2-105">DESCRIPTION</span></span>
<span data-ttu-id="4f1f2-106">A **Test-AzSynapseWorkspace** parancsmag ellenőrzi, hogy létezik-e Synapse Analytics-munkaterület.</span><span class="sxs-lookup"><span data-stu-id="4f1f2-106">The **Test-AzSynapseWorkspace** cmdlet checks for the existence of a Synapse Analytics workspace.</span></span>

## <span data-ttu-id="4f1f2-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="4f1f2-107">EXAMPLES</span></span>

### <span data-ttu-id="4f1f2-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="4f1f2-108">Example 1</span></span>
```powershell
PS C:\> Test-AzSynapseWorkspace -Name ContosoWorkspace
```

<span data-ttu-id="4f1f2-109">Ez a parancs ellenőrzi, hogy létezik-e Synapse Analytics-munkaterület.</span><span class="sxs-lookup"><span data-stu-id="4f1f2-109">This command checks for the existence of a Synapse Analytics workspace.</span></span>

## <span data-ttu-id="4f1f2-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4f1f2-110">PARAMETERS</span></span>

### <span data-ttu-id="4f1f2-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4f1f2-111">-DefaultProfile</span></span>
<span data-ttu-id="4f1f2-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="4f1f2-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4f1f2-113">-Name</span><span class="sxs-lookup"><span data-stu-id="4f1f2-113">-Name</span></span>
<span data-ttu-id="4f1f2-114">A Synapse-munkaterület neve.</span><span class="sxs-lookup"><span data-stu-id="4f1f2-114">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="4f1f2-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4f1f2-115">-ResourceGroupName</span></span>
<span data-ttu-id="4f1f2-116">Erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="4f1f2-116">Resource group name.</span></span>

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

### <span data-ttu-id="4f1f2-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4f1f2-117">CommonParameters</span></span>
<span data-ttu-id="4f1f2-118">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4f1f2-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4f1f2-119">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4f1f2-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4f1f2-120">INPUTS</span><span class="sxs-lookup"><span data-stu-id="4f1f2-120">INPUTS</span></span>

### <span data-ttu-id="4f1f2-121">Nincs</span><span class="sxs-lookup"><span data-stu-id="4f1f2-121">None</span></span>

## <span data-ttu-id="4f1f2-122">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4f1f2-122">OUTPUTS</span></span>

### <span data-ttu-id="4f1f2-123">System.Object</span><span class="sxs-lookup"><span data-stu-id="4f1f2-123">System.Object</span></span>
## <span data-ttu-id="4f1f2-124">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="4f1f2-124">NOTES</span></span>

## <span data-ttu-id="4f1f2-125">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4f1f2-125">RELATED LINKS</span></span>
