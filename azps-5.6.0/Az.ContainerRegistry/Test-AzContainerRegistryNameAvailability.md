---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/powershell/module/az.containerregistry/test-azcontainerregistrynameavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Test-AzContainerRegistryNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Test-AzContainerRegistryNameAvailability.md
ms.openlocfilehash: 0a0701a073101b0611f74a9443473fcd9568ca50
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101920785"
---
# <span data-ttu-id="deee2-101">Test-AzContainerRegistryNameAvailability</span><span class="sxs-lookup"><span data-stu-id="deee2-101">Test-AzContainerRegistryNameAvailability</span></span>

## <span data-ttu-id="deee2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="deee2-102">SYNOPSIS</span></span>
<span data-ttu-id="deee2-103">Egy tároló beállításjegyzék-nevének elérhetőségét ellenőrzi.</span><span class="sxs-lookup"><span data-stu-id="deee2-103">Checks the availability of a container registry name.</span></span>

## <span data-ttu-id="deee2-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="deee2-104">SYNTAX</span></span>

```
Test-AzContainerRegistryNameAvailability [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="deee2-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="deee2-105">DESCRIPTION</span></span>
<span data-ttu-id="deee2-106">A Test-AzContainerRegistryNameAvailability parancsmag ellenőrzi, hogy a tároló beállításjegyzékének neve érvényes-e és használható-e.</span><span class="sxs-lookup"><span data-stu-id="deee2-106">The Test-AzContainerRegistryNameAvailability cmdlet checks whether a container registry name is valid and available to use.</span></span>

## <span data-ttu-id="deee2-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="deee2-107">EXAMPLES</span></span>

### <span data-ttu-id="deee2-108">1. példa: A tároló beállításjegyzék-nevének elérhetőségét ellenőrzi</span><span class="sxs-lookup"><span data-stu-id="deee2-108">Example 1: Checks the availability of a container registry name</span></span>
```powershell
PS C:\>Test-AzContainerRegistryNameAvailability -Name 'SomeRegistryName'

NameAvailable Reason Message
------------- ------ -------
         True
```

<span data-ttu-id="deee2-109">Ez a parancs ellenőrzi, hogy rendelkezésre áll-e a \` SomeRegistryName nevű tárolóadatbázisnév. \`</span><span class="sxs-lookup"><span data-stu-id="deee2-109">This command checks the availability of the container registry name \`SomeRegistryName\`.</span></span>

## <span data-ttu-id="deee2-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="deee2-110">PARAMETERS</span></span>

### <span data-ttu-id="deee2-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="deee2-111">-DefaultProfile</span></span>
<span data-ttu-id="deee2-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="deee2-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="deee2-113">-Name</span><span class="sxs-lookup"><span data-stu-id="deee2-113">-Name</span></span>
<span data-ttu-id="deee2-114">Tároló beállításjegyzékének neve.</span><span class="sxs-lookup"><span data-stu-id="deee2-114">Container Registry Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ContainerRegistryName, RegistryName, ResourceName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="deee2-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="deee2-115">CommonParameters</span></span>
<span data-ttu-id="deee2-116">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="deee2-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="deee2-117">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="deee2-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="deee2-118">INPUTS</span><span class="sxs-lookup"><span data-stu-id="deee2-118">INPUTS</span></span>

### <span data-ttu-id="deee2-119">System.String</span><span class="sxs-lookup"><span data-stu-id="deee2-119">System.String</span></span>

## <span data-ttu-id="deee2-120">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="deee2-120">OUTPUTS</span></span>

### <span data-ttu-id="deee2-121">Microsoft.Azure.Management.ContainerRegistry.Models.RegistryNameStatus</span><span class="sxs-lookup"><span data-stu-id="deee2-121">Microsoft.Azure.Management.ContainerRegistry.Models.RegistryNameStatus</span></span>

## <span data-ttu-id="deee2-122">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="deee2-122">NOTES</span></span>

## <span data-ttu-id="deee2-123">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="deee2-123">RELATED LINKS</span></span>

[<span data-ttu-id="deee2-124">New-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="deee2-124">New-AzContainerRegistry</span></span>]()

