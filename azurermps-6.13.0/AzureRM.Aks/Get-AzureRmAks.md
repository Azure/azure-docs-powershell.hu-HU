---
external help file: Microsoft.Azure.Commands.Aks.dll-Help.xml
Module Name: AzureRM.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.aks/get-azurermaks
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Aks/Commands.Aks/help/Get-AzureRmAks.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Aks/Commands.Aks/help/Get-AzureRmAks.md
ms.openlocfilehash: d30d9858a3050864f5cc86601adf6b598be8c54d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93501271"
---
# <span data-ttu-id="e28a7-101">Get-AzureRmAks</span><span class="sxs-lookup"><span data-stu-id="e28a7-101">Get-AzureRmAks</span></span>

## <span data-ttu-id="e28a7-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e28a7-102">SYNOPSIS</span></span>
<span data-ttu-id="e28a7-103">Kubernetes felügyelt fürtök listája</span><span class="sxs-lookup"><span data-stu-id="e28a7-103">List Kubernetes managed clusters.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e28a7-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e28a7-104">SYNTAX</span></span>

### <span data-ttu-id="e28a7-105">ResourceGroupParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="e28a7-105">ResourceGroupParameterSet (Default)</span></span>
```
Get-AzureRmAks [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e28a7-106">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e28a7-106">IdParameterSet</span></span>
```
Get-AzureRmAks [-Id] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e28a7-107">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="e28a7-107">NameParameterSet</span></span>
```
Get-AzureRmAks [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e28a7-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="e28a7-108">DESCRIPTION</span></span>
<span data-ttu-id="e28a7-109">Kubernetes felügyelt fürtök listája</span><span class="sxs-lookup"><span data-stu-id="e28a7-109">List Kubernetes managed clusters.</span></span>

## <span data-ttu-id="e28a7-110">Példák</span><span class="sxs-lookup"><span data-stu-id="e28a7-110">EXAMPLES</span></span>

### <span data-ttu-id="e28a7-111">Az összes Kubernetes-halmaz listázása</span><span class="sxs-lookup"><span data-stu-id="e28a7-111">List all Kubernetes clusters</span></span>
```
PS C:\> Get-AzureRmAks
```

## <span data-ttu-id="e28a7-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e28a7-112">PARAMETERS</span></span>

### <span data-ttu-id="e28a7-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e28a7-113">-DefaultProfile</span></span>
<span data-ttu-id="e28a7-114">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e28a7-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e28a7-115">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="e28a7-115">-Id</span></span>
<span data-ttu-id="e28a7-116">Felügyelt Kubernetes-fürt azonosítója</span><span class="sxs-lookup"><span data-stu-id="e28a7-116">Id of a managed Kubernetes cluster</span></span>

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

### <span data-ttu-id="e28a7-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="e28a7-117">-Name</span></span>
<span data-ttu-id="e28a7-118">A felügyelt Kubernetes-fürt neve</span><span class="sxs-lookup"><span data-stu-id="e28a7-118">Name of your managed Kubernetes cluster</span></span>

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

### <span data-ttu-id="e28a7-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e28a7-119">-ResourceGroupName</span></span>
<span data-ttu-id="e28a7-120">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="e28a7-120">Resource group name</span></span>

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

### <span data-ttu-id="e28a7-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e28a7-121">CommonParameters</span></span>
<span data-ttu-id="e28a7-122">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e28a7-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e28a7-123">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e28a7-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e28a7-124">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e28a7-124">INPUTS</span></span>

### <span data-ttu-id="e28a7-125">System. String</span><span class="sxs-lookup"><span data-stu-id="e28a7-125">System.String</span></span>

## <span data-ttu-id="e28a7-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e28a7-126">OUTPUTS</span></span>

### <span data-ttu-id="e28a7-127">Microsoft. Azure. Command. AK. models. PSKubernetesCluster</span><span class="sxs-lookup"><span data-stu-id="e28a7-127">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

## <span data-ttu-id="e28a7-128">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e28a7-128">NOTES</span></span>

## <span data-ttu-id="e28a7-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e28a7-129">RELATED LINKS</span></span>
