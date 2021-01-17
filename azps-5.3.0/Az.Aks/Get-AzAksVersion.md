---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/az.aks/get-azaksversion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Get-AzAksVersion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Get-AzAksVersion.md
ms.openlocfilehash: 704e95cdd01291fb617a6f0c22a051daa69434d4
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98479122"
---
# <span data-ttu-id="0a16d-101">Get-AzAksVersion</span><span class="sxs-lookup"><span data-stu-id="0a16d-101">Get-AzAksVersion</span></span>

## <span data-ttu-id="0a16d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0a16d-102">SYNOPSIS</span></span>
<span data-ttu-id="0a16d-103">List available version for creating managed Kubernetes cluster.</span><span class="sxs-lookup"><span data-stu-id="0a16d-103">List available version for creating managed Kubernetes cluster.</span></span>

## <span data-ttu-id="0a16d-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="0a16d-104">SYNTAX</span></span>

```
Get-AzAksVersion -Location <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0a16d-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="0a16d-105">DESCRIPTION</span></span>
<span data-ttu-id="0a16d-106">List available version for creating managed Kubernetes cluster.</span><span class="sxs-lookup"><span data-stu-id="0a16d-106">List available version for creating managed Kubernetes cluster.</span></span>

## <span data-ttu-id="0a16d-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="0a16d-107">EXAMPLES</span></span>

### <span data-ttu-id="0a16d-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="0a16d-108">Example 1</span></span>
```powershell
PS C:\> Get-AzAksVersion -Location westus
```

## <span data-ttu-id="0a16d-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0a16d-109">PARAMETERS</span></span>

### <span data-ttu-id="0a16d-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0a16d-110">-DefaultProfile</span></span>
<span data-ttu-id="0a16d-111">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="0a16d-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0a16d-112">-Location</span><span class="sxs-lookup"><span data-stu-id="0a16d-112">-Location</span></span>
<span data-ttu-id="0a16d-113">A fürt Azure-helye.</span><span class="sxs-lookup"><span data-stu-id="0a16d-113">Azure location for the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a16d-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0a16d-114">CommonParameters</span></span>
<span data-ttu-id="0a16d-115">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0a16d-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0a16d-116">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0a16d-116">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0a16d-117">INPUTS</span><span class="sxs-lookup"><span data-stu-id="0a16d-117">INPUTS</span></span>

### <span data-ttu-id="0a16d-118">Nincs</span><span class="sxs-lookup"><span data-stu-id="0a16d-118">None</span></span>

## <span data-ttu-id="0a16d-119">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0a16d-119">OUTPUTS</span></span>

### <span data-ttu-id="0a16d-120">Microsoft.Azure.Commands.Aks.Models.PSOrchestratorVersionProfile</span><span class="sxs-lookup"><span data-stu-id="0a16d-120">Microsoft.Azure.Commands.Aks.Models.PSOrchestratorVersionProfile</span></span>

## <span data-ttu-id="0a16d-121">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="0a16d-121">NOTES</span></span>

## <span data-ttu-id="0a16d-122">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0a16d-122">RELATED LINKS</span></span>
