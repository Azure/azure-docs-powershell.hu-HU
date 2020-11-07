---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/az.aks/get-azaks
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Get-AzAks.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Get-AzAks.md
ms.openlocfilehash: 34db847ba7a4051efab32a62c667d3d79ad4ac30
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93668210"
---
# <span data-ttu-id="5edc1-101">Get-AzAks</span><span class="sxs-lookup"><span data-stu-id="5edc1-101">Get-AzAks</span></span>

## <span data-ttu-id="5edc1-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="5edc1-102">SYNOPSIS</span></span>
<span data-ttu-id="5edc1-103">Kubernetes felügyelt fürtök listája</span><span class="sxs-lookup"><span data-stu-id="5edc1-103">List Kubernetes managed clusters.</span></span>

## <span data-ttu-id="5edc1-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="5edc1-104">SYNTAX</span></span>

### <span data-ttu-id="5edc1-105">ResourceGroupParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="5edc1-105">ResourceGroupParameterSet (Default)</span></span>
```
Get-AzAks [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5edc1-106">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="5edc1-106">IdParameterSet</span></span>
```
Get-AzAks [-Id] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5edc1-107">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="5edc1-107">NameParameterSet</span></span>
```
Get-AzAks [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="5edc1-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="5edc1-108">DESCRIPTION</span></span>
<span data-ttu-id="5edc1-109">Kubernetes felügyelt fürtök listája</span><span class="sxs-lookup"><span data-stu-id="5edc1-109">List Kubernetes managed clusters.</span></span>

## <span data-ttu-id="5edc1-110">Példák</span><span class="sxs-lookup"><span data-stu-id="5edc1-110">EXAMPLES</span></span>

### <span data-ttu-id="5edc1-111">Az összes Kubernetes-halmaz listázása</span><span class="sxs-lookup"><span data-stu-id="5edc1-111">List all Kubernetes clusters</span></span>
```
PS C:\> Get-AzAks
```

## <span data-ttu-id="5edc1-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="5edc1-112">PARAMETERS</span></span>

### <span data-ttu-id="5edc1-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5edc1-113">-DefaultProfile</span></span>
<span data-ttu-id="5edc1-114">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="5edc1-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5edc1-115">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="5edc1-115">-Id</span></span>
<span data-ttu-id="5edc1-116">Felügyelt Kubernetes-fürt azonosítója</span><span class="sxs-lookup"><span data-stu-id="5edc1-116">Id of a managed Kubernetes cluster</span></span>

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

### <span data-ttu-id="5edc1-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="5edc1-117">-Name</span></span>
<span data-ttu-id="5edc1-118">A felügyelt Kubernetes-fürt neve</span><span class="sxs-lookup"><span data-stu-id="5edc1-118">Name of your managed Kubernetes cluster</span></span>

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

### <span data-ttu-id="5edc1-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5edc1-119">-ResourceGroupName</span></span>
<span data-ttu-id="5edc1-120">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="5edc1-120">Resource group name</span></span>

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

### <span data-ttu-id="5edc1-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5edc1-121">CommonParameters</span></span>
<span data-ttu-id="5edc1-122">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="5edc1-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5edc1-123">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5edc1-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5edc1-124">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="5edc1-124">INPUTS</span></span>

### <span data-ttu-id="5edc1-125">System. String</span><span class="sxs-lookup"><span data-stu-id="5edc1-125">System.String</span></span>

## <span data-ttu-id="5edc1-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5edc1-126">OUTPUTS</span></span>

### <span data-ttu-id="5edc1-127">Microsoft. Azure. Command. AK. models. PSKubernetesCluster</span><span class="sxs-lookup"><span data-stu-id="5edc1-127">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

## <span data-ttu-id="5edc1-128">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="5edc1-128">NOTES</span></span>

## <span data-ttu-id="5edc1-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5edc1-129">RELATED LINKS</span></span>
