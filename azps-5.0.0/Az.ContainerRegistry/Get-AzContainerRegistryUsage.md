---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/get-azcontainerregistryusage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Get-AzContainerRegistryUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Get-AzContainerRegistryUsage.md
ms.openlocfilehash: 691d8cf006e720d706d2473f76ff8660927e73ed
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94185582"
---
# <span data-ttu-id="d3e97-101">Get-AzContainerRegistryUsage</span><span class="sxs-lookup"><span data-stu-id="d3e97-101">Get-AzContainerRegistryUsage</span></span>

## <span data-ttu-id="d3e97-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d3e97-102">SYNOPSIS</span></span>
<span data-ttu-id="d3e97-103">Az Azure Container-regisztrációk használatának megkezdése</span><span class="sxs-lookup"><span data-stu-id="d3e97-103">Get Usage of an azure container registry.</span></span>

## <span data-ttu-id="d3e97-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d3e97-104">SYNTAX</span></span>

```
Get-AzContainerRegistryUsage -ResourceGroupName <String> -RegistryName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d3e97-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="d3e97-105">DESCRIPTION</span></span>
<span data-ttu-id="d3e97-106">Az Azure Container-regisztrációk használatának megkezdése</span><span class="sxs-lookup"><span data-stu-id="d3e97-106">Get Usage of an azure container registry.</span></span>

## <span data-ttu-id="d3e97-107">Példák</span><span class="sxs-lookup"><span data-stu-id="d3e97-107">EXAMPLES</span></span>

### <span data-ttu-id="d3e97-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="d3e97-108">Example 1</span></span>
```powershell
PS C:\> Get-AzContainerRegistryUsage -ResourceGroupName $resourceGroupName -RegistryName $RegistryName
```

<span data-ttu-id="d3e97-109">Az Azure Container-regisztrációk használatának megkezdése</span><span class="sxs-lookup"><span data-stu-id="d3e97-109">Get Usage of an azure container registry.</span></span>

## <span data-ttu-id="d3e97-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d3e97-110">PARAMETERS</span></span>

### <span data-ttu-id="d3e97-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d3e97-111">-DefaultProfile</span></span>
<span data-ttu-id="d3e97-112">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d3e97-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d3e97-113">-RegistryName</span><span class="sxs-lookup"><span data-stu-id="d3e97-113">-RegistryName</span></span>
<span data-ttu-id="d3e97-114">A cél beállításjegyzékének neve.</span><span class="sxs-lookup"><span data-stu-id="d3e97-114">Target registry name.</span></span>

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

### <span data-ttu-id="d3e97-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d3e97-115">-ResourceGroupName</span></span>
<span data-ttu-id="d3e97-116">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="d3e97-116">Resource group name.</span></span>

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

### <span data-ttu-id="d3e97-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d3e97-117">CommonParameters</span></span>
<span data-ttu-id="d3e97-118">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d3e97-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d3e97-119">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="d3e97-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d3e97-120">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d3e97-120">INPUTS</span></span>

### <span data-ttu-id="d3e97-121">System. String</span><span class="sxs-lookup"><span data-stu-id="d3e97-121">System.String</span></span>

## <span data-ttu-id="d3e97-122">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d3e97-122">OUTPUTS</span></span>

### <span data-ttu-id="d3e97-123">Microsoft. Azure. Command. ContainerRegistry. models. PSRegistryUsage</span><span class="sxs-lookup"><span data-stu-id="d3e97-123">Microsoft.Azure.Commands.ContainerRegistry.Models.PSRegistryUsage</span></span>

## <span data-ttu-id="d3e97-124">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d3e97-124">NOTES</span></span>

## <span data-ttu-id="d3e97-125">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d3e97-125">RELATED LINKS</span></span>
