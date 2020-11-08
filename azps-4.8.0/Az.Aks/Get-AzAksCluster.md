---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/az.aks/get-azakscluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Get-AzAksCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Get-AzAksCluster.md
ms.openlocfilehash: d2702c28a4cedc0198f3fb767f0e509912269a63
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94183414"
---
# <span data-ttu-id="8fc86-101">Get-AzAksCluster</span><span class="sxs-lookup"><span data-stu-id="8fc86-101">Get-AzAksCluster</span></span>

## <span data-ttu-id="8fc86-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="8fc86-102">SYNOPSIS</span></span>
<span data-ttu-id="8fc86-103">Kubernetes felügyelt fürtök listája</span><span class="sxs-lookup"><span data-stu-id="8fc86-103">List Kubernetes managed clusters.</span></span>

## <span data-ttu-id="8fc86-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="8fc86-104">SYNTAX</span></span>

### <span data-ttu-id="8fc86-105">ResourceGroupParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="8fc86-105">ResourceGroupParameterSet (Default)</span></span>
```
Get-AzAksCluster [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="8fc86-106">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8fc86-106">IdParameterSet</span></span>
```
Get-AzAksCluster [-Id] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8fc86-107">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="8fc86-107">NameParameterSet</span></span>
```
Get-AzAksCluster [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="8fc86-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="8fc86-108">DESCRIPTION</span></span>
<span data-ttu-id="8fc86-109">Kubernetes felügyelt fürtök listája</span><span class="sxs-lookup"><span data-stu-id="8fc86-109">List Kubernetes managed clusters.</span></span>

## <span data-ttu-id="8fc86-110">Példák</span><span class="sxs-lookup"><span data-stu-id="8fc86-110">EXAMPLES</span></span>

### <span data-ttu-id="8fc86-111">Az összes Kubernetes-halmaz listázása</span><span class="sxs-lookup"><span data-stu-id="8fc86-111">List all Kubernetes clusters</span></span>
```powershell
PS C:\> Get-AzAksCluster
```

## <span data-ttu-id="8fc86-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="8fc86-112">PARAMETERS</span></span>

### <span data-ttu-id="8fc86-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8fc86-113">-DefaultProfile</span></span>
<span data-ttu-id="8fc86-114">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="8fc86-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8fc86-115">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="8fc86-115">-Id</span></span>
<span data-ttu-id="8fc86-116">Felügyelt Kubernetes-fürt azonosítója</span><span class="sxs-lookup"><span data-stu-id="8fc86-116">Id of a managed Kubernetes cluster</span></span>

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

### <span data-ttu-id="8fc86-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="8fc86-117">-Name</span></span>
<span data-ttu-id="8fc86-118">A felügyelt Kubernetes-fürt neve</span><span class="sxs-lookup"><span data-stu-id="8fc86-118">Name of your managed Kubernetes cluster</span></span>

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

### <span data-ttu-id="8fc86-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8fc86-119">-ResourceGroupName</span></span>
<span data-ttu-id="8fc86-120">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="8fc86-120">Resource group name</span></span>

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

### <span data-ttu-id="8fc86-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8fc86-121">CommonParameters</span></span>
<span data-ttu-id="8fc86-122">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="8fc86-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8fc86-123">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="8fc86-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8fc86-124">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="8fc86-124">INPUTS</span></span>

### <span data-ttu-id="8fc86-125">System. String</span><span class="sxs-lookup"><span data-stu-id="8fc86-125">System.String</span></span>

## <span data-ttu-id="8fc86-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8fc86-126">OUTPUTS</span></span>

### <span data-ttu-id="8fc86-127">Microsoft. Azure. Command. AK. models. PSKubernetesCluster</span><span class="sxs-lookup"><span data-stu-id="8fc86-127">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

## <span data-ttu-id="8fc86-128">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="8fc86-128">NOTES</span></span>

## <span data-ttu-id="8fc86-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8fc86-129">RELATED LINKS</span></span>
