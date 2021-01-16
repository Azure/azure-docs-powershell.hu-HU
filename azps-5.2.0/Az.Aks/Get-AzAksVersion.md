---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/az.aks/get-azaksversion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Get-AzAksVersion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Get-AzAksVersion.md
ms.openlocfilehash: 704e95cdd01291fb617a6f0c22a051daa69434d4
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98356508"
---
# <span data-ttu-id="1299c-101">Get-AzAksVersion</span><span class="sxs-lookup"><span data-stu-id="1299c-101">Get-AzAksVersion</span></span>

## <span data-ttu-id="1299c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1299c-102">SYNOPSIS</span></span>
<span data-ttu-id="1299c-103">List available version for creating managed Kubernetes cluster.</span><span class="sxs-lookup"><span data-stu-id="1299c-103">List available version for creating managed Kubernetes cluster.</span></span>

## <span data-ttu-id="1299c-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="1299c-104">SYNTAX</span></span>

```
Get-AzAksVersion -Location <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1299c-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="1299c-105">DESCRIPTION</span></span>
<span data-ttu-id="1299c-106">List available version for creating managed Kubernetes cluster.</span><span class="sxs-lookup"><span data-stu-id="1299c-106">List available version for creating managed Kubernetes cluster.</span></span>

## <span data-ttu-id="1299c-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="1299c-107">EXAMPLES</span></span>

### <span data-ttu-id="1299c-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="1299c-108">Example 1</span></span>
```powershell
PS C:\> Get-AzAksVersion -Location westus
```

## <span data-ttu-id="1299c-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1299c-109">PARAMETERS</span></span>

### <span data-ttu-id="1299c-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1299c-110">-DefaultProfile</span></span>
<span data-ttu-id="1299c-111">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="1299c-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1299c-112">-Location</span><span class="sxs-lookup"><span data-stu-id="1299c-112">-Location</span></span>
<span data-ttu-id="1299c-113">A fürt Azure-helye.</span><span class="sxs-lookup"><span data-stu-id="1299c-113">Azure location for the cluster.</span></span>

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

### <span data-ttu-id="1299c-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1299c-114">CommonParameters</span></span>
<span data-ttu-id="1299c-115">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1299c-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1299c-116">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1299c-116">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1299c-117">INPUTS</span><span class="sxs-lookup"><span data-stu-id="1299c-117">INPUTS</span></span>

### <span data-ttu-id="1299c-118">Nincs</span><span class="sxs-lookup"><span data-stu-id="1299c-118">None</span></span>

## <span data-ttu-id="1299c-119">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1299c-119">OUTPUTS</span></span>

### <span data-ttu-id="1299c-120">Microsoft.Azure.Commands.Aks.Models.PSOrchestratorVersionProfile</span><span class="sxs-lookup"><span data-stu-id="1299c-120">Microsoft.Azure.Commands.Aks.Models.PSOrchestratorVersionProfile</span></span>

## <span data-ttu-id="1299c-121">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="1299c-121">NOTES</span></span>

## <span data-ttu-id="1299c-122">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1299c-122">RELATED LINKS</span></span>
