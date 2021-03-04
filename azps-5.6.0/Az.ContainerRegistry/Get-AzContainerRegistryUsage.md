---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/powershell/module/az.containerregistry/get-azcontainerregistryusage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Get-AzContainerRegistryUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Get-AzContainerRegistryUsage.md
ms.openlocfilehash: 7a950bc3b375ea9d86ef71eda120ac1d92fbd8e9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101938217"
---
# <span data-ttu-id="e6490-101">Get-AzContainerRegistryUsage</span><span class="sxs-lookup"><span data-stu-id="e6490-101">Get-AzContainerRegistryUsage</span></span>

## <span data-ttu-id="e6490-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e6490-102">SYNOPSIS</span></span>
<span data-ttu-id="e6490-103">Azure container registry használatának lekérte.</span><span class="sxs-lookup"><span data-stu-id="e6490-103">Get Usage of an azure container registry.</span></span>

## <span data-ttu-id="e6490-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="e6490-104">SYNTAX</span></span>

```
Get-AzContainerRegistryUsage -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e6490-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="e6490-105">DESCRIPTION</span></span>
<span data-ttu-id="e6490-106">Azure container registry használatának lekérte.</span><span class="sxs-lookup"><span data-stu-id="e6490-106">Get Usage of an azure container registry.</span></span>

## <span data-ttu-id="e6490-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="e6490-107">EXAMPLES</span></span>

### <span data-ttu-id="e6490-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="e6490-108">Example 1</span></span>
```powershell
PS C:\> Get-AzContainerRegistryUsage -ResourceGroupName $resourceGroupName -RegistryName $RegistryName
```

<span data-ttu-id="e6490-109">Azure container registry használatának lekérte.</span><span class="sxs-lookup"><span data-stu-id="e6490-109">Get Usage of an azure container registry.</span></span>

## <span data-ttu-id="e6490-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e6490-110">PARAMETERS</span></span>

### <span data-ttu-id="e6490-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e6490-111">-DefaultProfile</span></span>
<span data-ttu-id="e6490-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e6490-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e6490-113">-Name</span><span class="sxs-lookup"><span data-stu-id="e6490-113">-Name</span></span>
<span data-ttu-id="e6490-114">Cél beállításjegyzék neve.</span><span class="sxs-lookup"><span data-stu-id="e6490-114">Target registry name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: RegistryName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e6490-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e6490-115">-ResourceGroupName</span></span>
<span data-ttu-id="e6490-116">Erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="e6490-116">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e6490-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e6490-117">CommonParameters</span></span>
<span data-ttu-id="e6490-118">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e6490-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e6490-119">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e6490-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e6490-120">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e6490-120">INPUTS</span></span>

### <span data-ttu-id="e6490-121">System.String</span><span class="sxs-lookup"><span data-stu-id="e6490-121">System.String</span></span>

## <span data-ttu-id="e6490-122">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e6490-122">OUTPUTS</span></span>

### <span data-ttu-id="e6490-123">Microsoft.Azure.Commands.ContainerRegistry.Models.PSRegistryUsage</span><span class="sxs-lookup"><span data-stu-id="e6490-123">Microsoft.Azure.Commands.ContainerRegistry.Models.PSRegistryUsage</span></span>

## <span data-ttu-id="e6490-124">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="e6490-124">NOTES</span></span>

## <span data-ttu-id="e6490-125">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e6490-125">RELATED LINKS</span></span>
