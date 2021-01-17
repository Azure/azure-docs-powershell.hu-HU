---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/az.aks/get-azakscluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Get-AzAksCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Get-AzAksCluster.md
ms.openlocfilehash: d2702c28a4cedc0198f3fb767f0e509912269a63
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98342485"
---
# <span data-ttu-id="86857-101">Get-AzAksCluster</span><span class="sxs-lookup"><span data-stu-id="86857-101">Get-AzAksCluster</span></span>

## <span data-ttu-id="86857-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="86857-102">SYNOPSIS</span></span>
<span data-ttu-id="86857-103">List Kutbernetes felügyelt fürtök.</span><span class="sxs-lookup"><span data-stu-id="86857-103">List Kubernetes managed clusters.</span></span>

## <span data-ttu-id="86857-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="86857-104">SYNTAX</span></span>

### <span data-ttu-id="86857-105">ResourceGroupParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="86857-105">ResourceGroupParameterSet (Default)</span></span>
```
Get-AzAksCluster [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="86857-106">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="86857-106">IdParameterSet</span></span>
```
Get-AzAksCluster [-Id] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="86857-107">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="86857-107">NameParameterSet</span></span>
```
Get-AzAksCluster [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="86857-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="86857-108">DESCRIPTION</span></span>
<span data-ttu-id="86857-109">List Kutbernetes felügyelt fürtök.</span><span class="sxs-lookup"><span data-stu-id="86857-109">List Kubernetes managed clusters.</span></span>

## <span data-ttu-id="86857-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="86857-110">EXAMPLES</span></span>

### <span data-ttu-id="86857-111">Az összes Kubanetes-fürt felsorolása</span><span class="sxs-lookup"><span data-stu-id="86857-111">List all Kubernetes clusters</span></span>
```powershell
PS C:\> Get-AzAksCluster
```

## <span data-ttu-id="86857-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="86857-112">PARAMETERS</span></span>

### <span data-ttu-id="86857-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="86857-113">-DefaultProfile</span></span>
<span data-ttu-id="86857-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="86857-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="86857-115">-Id</span><span class="sxs-lookup"><span data-stu-id="86857-115">-Id</span></span>
<span data-ttu-id="86857-116">Felügyelt Kubanetes-fürt azonosítója</span><span class="sxs-lookup"><span data-stu-id="86857-116">Id of a managed Kubernetes cluster</span></span>

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

### <span data-ttu-id="86857-117">-Name</span><span class="sxs-lookup"><span data-stu-id="86857-117">-Name</span></span>
<span data-ttu-id="86857-118">A felügyelt Kubanetes-fürt neve</span><span class="sxs-lookup"><span data-stu-id="86857-118">Name of your managed Kubernetes cluster</span></span>

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

### <span data-ttu-id="86857-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="86857-119">-ResourceGroupName</span></span>
<span data-ttu-id="86857-120">Erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="86857-120">Resource group name</span></span>

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

### <span data-ttu-id="86857-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="86857-121">CommonParameters</span></span>
<span data-ttu-id="86857-122">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="86857-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="86857-123">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="86857-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="86857-124">INPUTS</span><span class="sxs-lookup"><span data-stu-id="86857-124">INPUTS</span></span>

### <span data-ttu-id="86857-125">System.String</span><span class="sxs-lookup"><span data-stu-id="86857-125">System.String</span></span>

## <span data-ttu-id="86857-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="86857-126">OUTPUTS</span></span>

### <span data-ttu-id="86857-127">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span><span class="sxs-lookup"><span data-stu-id="86857-127">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

## <span data-ttu-id="86857-128">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="86857-128">NOTES</span></span>

## <span data-ttu-id="86857-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="86857-129">RELATED LINKS</span></span>
