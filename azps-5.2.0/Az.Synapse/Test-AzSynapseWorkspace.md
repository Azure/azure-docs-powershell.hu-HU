---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/test-azsynapseworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Test-AzSynapseWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Test-AzSynapseWorkspace.md
ms.openlocfilehash: b3dd32ec177aaa38e8fbb1f66559592f84905f2d
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98339821"
---
# <span data-ttu-id="3e48a-101">Test-AzSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="3e48a-101">Test-AzSynapseWorkspace</span></span>

## <span data-ttu-id="3e48a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3e48a-102">SYNOPSIS</span></span>
<span data-ttu-id="3e48a-103">Ellenőrzi, hogy létezik-e Synapse Analytics-munkaterület.</span><span class="sxs-lookup"><span data-stu-id="3e48a-103">Checks for the existence of a Synapse Analytics workspace.</span></span>

## <span data-ttu-id="3e48a-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="3e48a-104">SYNTAX</span></span>

```
Test-AzSynapseWorkspace [-Name] <String> [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3e48a-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="3e48a-105">DESCRIPTION</span></span>
<span data-ttu-id="3e48a-106">A **Test-AzSynapseWorkspace** parancsmag ellenőrzi, hogy létezik-e Synapse Analytics-munkaterület.</span><span class="sxs-lookup"><span data-stu-id="3e48a-106">The **Test-AzSynapseWorkspace** cmdlet checks for the existence of a Synapse Analytics workspace.</span></span>

## <span data-ttu-id="3e48a-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="3e48a-107">EXAMPLES</span></span>

### <span data-ttu-id="3e48a-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="3e48a-108">Example 1</span></span>
```powershell
PS C:\> Test-AzSynapseWorkspace -Name ContosoWorkspace
```

<span data-ttu-id="3e48a-109">Ez a parancs ellenőrzi, hogy létezik-e Synapse Analytics-munkaterület.</span><span class="sxs-lookup"><span data-stu-id="3e48a-109">This command checks for the existence of a Synapse Analytics workspace.</span></span>

## <span data-ttu-id="3e48a-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3e48a-110">PARAMETERS</span></span>

### <span data-ttu-id="3e48a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3e48a-111">-DefaultProfile</span></span>
<span data-ttu-id="3e48a-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="3e48a-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3e48a-113">-Name</span><span class="sxs-lookup"><span data-stu-id="3e48a-113">-Name</span></span>
<span data-ttu-id="3e48a-114">A Synapse-munkaterület neve.</span><span class="sxs-lookup"><span data-stu-id="3e48a-114">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="3e48a-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3e48a-115">-ResourceGroupName</span></span>
<span data-ttu-id="3e48a-116">Erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="3e48a-116">Resource group name.</span></span>

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

### <span data-ttu-id="3e48a-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3e48a-117">CommonParameters</span></span>
<span data-ttu-id="3e48a-118">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3e48a-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3e48a-119">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3e48a-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3e48a-120">INPUTS</span><span class="sxs-lookup"><span data-stu-id="3e48a-120">INPUTS</span></span>

### <span data-ttu-id="3e48a-121">Nincs</span><span class="sxs-lookup"><span data-stu-id="3e48a-121">None</span></span>

## <span data-ttu-id="3e48a-122">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3e48a-122">OUTPUTS</span></span>

### <span data-ttu-id="3e48a-123">System.Object</span><span class="sxs-lookup"><span data-stu-id="3e48a-123">System.Object</span></span>
## <span data-ttu-id="3e48a-124">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="3e48a-124">NOTES</span></span>

## <span data-ttu-id="3e48a-125">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3e48a-125">RELATED LINKS</span></span>
