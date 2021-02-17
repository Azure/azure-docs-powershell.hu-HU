---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/test-azsynapseworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Test-AzSynapseWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Test-AzSynapseWorkspace.md
ms.openlocfilehash: b3dd32ec177aaa38e8fbb1f66559592f84905f2d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100207583"
---
# <span data-ttu-id="0a777-101">Test-AzSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="0a777-101">Test-AzSynapseWorkspace</span></span>

## <span data-ttu-id="0a777-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0a777-102">SYNOPSIS</span></span>
<span data-ttu-id="0a777-103">Ellenőrzi, hogy létezik-e Synapse Analytics-munkaterület.</span><span class="sxs-lookup"><span data-stu-id="0a777-103">Checks for the existence of a Synapse Analytics workspace.</span></span>

## <span data-ttu-id="0a777-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="0a777-104">SYNTAX</span></span>

```
Test-AzSynapseWorkspace [-Name] <String> [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0a777-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="0a777-105">DESCRIPTION</span></span>
<span data-ttu-id="0a777-106">A **Test-AzSynapseWorkspace** parancsmag ellenőrzi, hogy létezik-e Synapse Analytics-munkaterület.</span><span class="sxs-lookup"><span data-stu-id="0a777-106">The **Test-AzSynapseWorkspace** cmdlet checks for the existence of a Synapse Analytics workspace.</span></span>

## <span data-ttu-id="0a777-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="0a777-107">EXAMPLES</span></span>

### <span data-ttu-id="0a777-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="0a777-108">Example 1</span></span>
```powershell
PS C:\> Test-AzSynapseWorkspace -Name ContosoWorkspace
```

<span data-ttu-id="0a777-109">Ez a parancs ellenőrzi, hogy létezik-e Synapse Analytics-munkaterület.</span><span class="sxs-lookup"><span data-stu-id="0a777-109">This command checks for the existence of a Synapse Analytics workspace.</span></span>

## <span data-ttu-id="0a777-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0a777-110">PARAMETERS</span></span>

### <span data-ttu-id="0a777-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0a777-111">-DefaultProfile</span></span>
<span data-ttu-id="0a777-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="0a777-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0a777-113">-Name</span><span class="sxs-lookup"><span data-stu-id="0a777-113">-Name</span></span>
<span data-ttu-id="0a777-114">A Synapse-munkaterület neve.</span><span class="sxs-lookup"><span data-stu-id="0a777-114">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="0a777-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0a777-115">-ResourceGroupName</span></span>
<span data-ttu-id="0a777-116">Erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="0a777-116">Resource group name.</span></span>

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

### <span data-ttu-id="0a777-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0a777-117">CommonParameters</span></span>
<span data-ttu-id="0a777-118">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0a777-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0a777-119">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0a777-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0a777-120">INPUTS</span><span class="sxs-lookup"><span data-stu-id="0a777-120">INPUTS</span></span>

### <span data-ttu-id="0a777-121">Nincs</span><span class="sxs-lookup"><span data-stu-id="0a777-121">None</span></span>

## <span data-ttu-id="0a777-122">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0a777-122">OUTPUTS</span></span>

### <span data-ttu-id="0a777-123">System.Object</span><span class="sxs-lookup"><span data-stu-id="0a777-123">System.Object</span></span>
## <span data-ttu-id="0a777-124">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="0a777-124">NOTES</span></span>

## <span data-ttu-id="0a777-125">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0a777-125">RELATED LINKS</span></span>
