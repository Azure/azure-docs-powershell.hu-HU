---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/az.aks/get-azaksversion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Get-AzAksVersion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Get-AzAksVersion.md
ms.openlocfilehash: 704e95cdd01291fb617a6f0c22a051daa69434d4
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94183412"
---
# <span data-ttu-id="fb16f-101">Get-AzAksVersion</span><span class="sxs-lookup"><span data-stu-id="fb16f-101">Get-AzAksVersion</span></span>

## <span data-ttu-id="fb16f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="fb16f-102">SYNOPSIS</span></span>
<span data-ttu-id="fb16f-103">Az elérhető verzió listája a felügyelt Kubernetes-fürtök létrehozásához.</span><span class="sxs-lookup"><span data-stu-id="fb16f-103">List available version for creating managed Kubernetes cluster.</span></span>

## <span data-ttu-id="fb16f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="fb16f-104">SYNTAX</span></span>

```
Get-AzAksVersion -Location <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fb16f-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="fb16f-105">DESCRIPTION</span></span>
<span data-ttu-id="fb16f-106">Az elérhető verzió listája a felügyelt Kubernetes-fürtök létrehozásához.</span><span class="sxs-lookup"><span data-stu-id="fb16f-106">List available version for creating managed Kubernetes cluster.</span></span>

## <span data-ttu-id="fb16f-107">Példák</span><span class="sxs-lookup"><span data-stu-id="fb16f-107">EXAMPLES</span></span>

### <span data-ttu-id="fb16f-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="fb16f-108">Example 1</span></span>
```powershell
PS C:\> Get-AzAksVersion -Location westus
```

## <span data-ttu-id="fb16f-109">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="fb16f-109">PARAMETERS</span></span>

### <span data-ttu-id="fb16f-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fb16f-110">-DefaultProfile</span></span>
<span data-ttu-id="fb16f-111">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="fb16f-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fb16f-112">-Hely</span><span class="sxs-lookup"><span data-stu-id="fb16f-112">-Location</span></span>
<span data-ttu-id="fb16f-113">A fürt Azure-helye.</span><span class="sxs-lookup"><span data-stu-id="fb16f-113">Azure location for the cluster.</span></span>

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

### <span data-ttu-id="fb16f-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fb16f-114">CommonParameters</span></span>
<span data-ttu-id="fb16f-115">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="fb16f-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fb16f-116">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="fb16f-116">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fb16f-117">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="fb16f-117">INPUTS</span></span>

### <span data-ttu-id="fb16f-118">Nincs</span><span class="sxs-lookup"><span data-stu-id="fb16f-118">None</span></span>

## <span data-ttu-id="fb16f-119">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="fb16f-119">OUTPUTS</span></span>

### <span data-ttu-id="fb16f-120">Microsoft. Azure. Command. AK. models. PSOrchestratorVersionProfile</span><span class="sxs-lookup"><span data-stu-id="fb16f-120">Microsoft.Azure.Commands.Aks.Models.PSOrchestratorVersionProfile</span></span>

## <span data-ttu-id="fb16f-121">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="fb16f-121">NOTES</span></span>

## <span data-ttu-id="fb16f-122">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="fb16f-122">RELATED LINKS</span></span>
