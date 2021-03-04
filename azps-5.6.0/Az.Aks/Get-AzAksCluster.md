---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/powershell/module/az.aks/get-azakscluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Get-AzAksCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Get-AzAksCluster.md
ms.openlocfilehash: 50d4dc8531f28ebb50ef562321b3974c7b50a102
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101926082"
---
# <span data-ttu-id="00733-101">Get-AzAksCluster</span><span class="sxs-lookup"><span data-stu-id="00733-101">Get-AzAksCluster</span></span>

## <span data-ttu-id="00733-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="00733-102">SYNOPSIS</span></span>
<span data-ttu-id="00733-103">List Kutbernetes felügyelt fürtök.</span><span class="sxs-lookup"><span data-stu-id="00733-103">List Kubernetes managed clusters.</span></span>

## <span data-ttu-id="00733-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="00733-104">SYNTAX</span></span>

### <span data-ttu-id="00733-105">ResourceGroupParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="00733-105">ResourceGroupParameterSet (Default)</span></span>
```
Get-AzAksCluster [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="00733-106">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="00733-106">IdParameterSet</span></span>
```
Get-AzAksCluster [-Id] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="00733-107">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="00733-107">NameParameterSet</span></span>
```
Get-AzAksCluster [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="00733-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="00733-108">DESCRIPTION</span></span>
<span data-ttu-id="00733-109">List Kutbernetes felügyelt fürtök.</span><span class="sxs-lookup"><span data-stu-id="00733-109">List Kubernetes managed clusters.</span></span>

## <span data-ttu-id="00733-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="00733-110">EXAMPLES</span></span>

### <span data-ttu-id="00733-111">Az összes Kubanetes-fürt felsorolása</span><span class="sxs-lookup"><span data-stu-id="00733-111">List all Kubernetes clusters</span></span>
```powershell
PS C:\> Get-AzAksCluster
```

## <span data-ttu-id="00733-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="00733-112">PARAMETERS</span></span>

### <span data-ttu-id="00733-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="00733-113">-DefaultProfile</span></span>
<span data-ttu-id="00733-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="00733-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="00733-115">-Id</span><span class="sxs-lookup"><span data-stu-id="00733-115">-Id</span></span>
<span data-ttu-id="00733-116">Felügyelt Kubanetes-fürt azonosítója</span><span class="sxs-lookup"><span data-stu-id="00733-116">Id of a managed Kubernetes cluster</span></span>

```yaml
Type: System.String
Parameter Sets: IdParameterSet
Aliases: ResourceId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="00733-117">-Name</span><span class="sxs-lookup"><span data-stu-id="00733-117">-Name</span></span>
<span data-ttu-id="00733-118">A felügyelt Kubanetes-fürt neve</span><span class="sxs-lookup"><span data-stu-id="00733-118">Name of your managed Kubernetes cluster</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="00733-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="00733-119">-ResourceGroupName</span></span>
<span data-ttu-id="00733-120">Erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="00733-120">Resource group name</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: NameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="00733-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="00733-121">CommonParameters</span></span>
<span data-ttu-id="00733-122">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="00733-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="00733-123">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="00733-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="00733-124">INPUTS</span><span class="sxs-lookup"><span data-stu-id="00733-124">INPUTS</span></span>

### <span data-ttu-id="00733-125">System.String</span><span class="sxs-lookup"><span data-stu-id="00733-125">System.String</span></span>

## <span data-ttu-id="00733-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="00733-126">OUTPUTS</span></span>

### <span data-ttu-id="00733-127">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span><span class="sxs-lookup"><span data-stu-id="00733-127">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

## <span data-ttu-id="00733-128">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="00733-128">NOTES</span></span>

## <span data-ttu-id="00733-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="00733-129">RELATED LINKS</span></span>
