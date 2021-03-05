---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/test-azsynapseworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Test-AzSynapseWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Test-AzSynapseWorkspace.md
ms.openlocfilehash: e92b4d20e89df451c483bc0b4bdccb83fdc8a140
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102011205"
---
# <span data-ttu-id="f7711-101">Test-AzSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="f7711-101">Test-AzSynapseWorkspace</span></span>

## <span data-ttu-id="f7711-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f7711-102">SYNOPSIS</span></span>
<span data-ttu-id="f7711-103">Ellenőrzi, hogy létezik-e Synapse Analytics-munkaterület.</span><span class="sxs-lookup"><span data-stu-id="f7711-103">Checks for the existence of a Synapse Analytics workspace.</span></span>

## <span data-ttu-id="f7711-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="f7711-104">SYNTAX</span></span>

```
Test-AzSynapseWorkspace [-Name] <String> [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f7711-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="f7711-105">DESCRIPTION</span></span>
<span data-ttu-id="f7711-106">A **Test-AzSynapseWorkspace** parancsmag ellenőrzi, hogy létezik-e Synapse Analytics-munkaterület.</span><span class="sxs-lookup"><span data-stu-id="f7711-106">The **Test-AzSynapseWorkspace** cmdlet checks for the existence of a Synapse Analytics workspace.</span></span>

## <span data-ttu-id="f7711-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="f7711-107">EXAMPLES</span></span>

### <span data-ttu-id="f7711-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="f7711-108">Example 1</span></span>
```powershell
PS C:\> Test-AzSynapseWorkspace -Name ContosoWorkspace
```

<span data-ttu-id="f7711-109">Ez a parancs ellenőrzi, hogy létezik-e Synapse Analytics-munkaterület.</span><span class="sxs-lookup"><span data-stu-id="f7711-109">This command checks for the existence of a Synapse Analytics workspace.</span></span>

## <span data-ttu-id="f7711-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f7711-110">PARAMETERS</span></span>

### <span data-ttu-id="f7711-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f7711-111">-DefaultProfile</span></span>
<span data-ttu-id="f7711-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f7711-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f7711-113">-Name</span><span class="sxs-lookup"><span data-stu-id="f7711-113">-Name</span></span>
<span data-ttu-id="f7711-114">A Synapse-munkaterület neve.</span><span class="sxs-lookup"><span data-stu-id="f7711-114">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="f7711-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f7711-115">-ResourceGroupName</span></span>
<span data-ttu-id="f7711-116">Erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="f7711-116">Resource group name.</span></span>

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

### <span data-ttu-id="f7711-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f7711-117">CommonParameters</span></span>
<span data-ttu-id="f7711-118">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f7711-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f7711-119">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f7711-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f7711-120">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f7711-120">INPUTS</span></span>

### <span data-ttu-id="f7711-121">Nincs</span><span class="sxs-lookup"><span data-stu-id="f7711-121">None</span></span>

## <span data-ttu-id="f7711-122">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f7711-122">OUTPUTS</span></span>

### <span data-ttu-id="f7711-123">System.Object</span><span class="sxs-lookup"><span data-stu-id="f7711-123">System.Object</span></span>
## <span data-ttu-id="f7711-124">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="f7711-124">NOTES</span></span>

## <span data-ttu-id="f7711-125">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f7711-125">RELATED LINKS</span></span>
