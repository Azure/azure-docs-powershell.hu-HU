---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/test-azcontainerregistrynameavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Test-AzContainerRegistryNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Test-AzContainerRegistryNameAvailability.md
ms.openlocfilehash: 153ed152c68444327f379fda9ab5009290cbc00a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100166323"
---
# <span data-ttu-id="7326f-101">Test-AzContainerRegistryNameAvailability</span><span class="sxs-lookup"><span data-stu-id="7326f-101">Test-AzContainerRegistryNameAvailability</span></span>

## <span data-ttu-id="7326f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7326f-102">SYNOPSIS</span></span>
<span data-ttu-id="7326f-103">Egy tároló beállításjegyzék-nevének elérhetőségét ellenőrzi.</span><span class="sxs-lookup"><span data-stu-id="7326f-103">Checks the availability of a container registry name.</span></span>

## <span data-ttu-id="7326f-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="7326f-104">SYNTAX</span></span>

```
Test-AzContainerRegistryNameAvailability [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="7326f-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="7326f-105">DESCRIPTION</span></span>
<span data-ttu-id="7326f-106">A Test-AzContainerRegistryNameAvailability parancsmag ellenőrzi, hogy egy tároló beállításjegyzék-neve érvényes-e és használható-e.</span><span class="sxs-lookup"><span data-stu-id="7326f-106">The Test-AzContainerRegistryNameAvailability cmdlet checks whether a container registry name is valid and available to use.</span></span>

## <span data-ttu-id="7326f-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="7326f-107">EXAMPLES</span></span>

### <span data-ttu-id="7326f-108">1. példa: A tároló beállításjegyzék-nevének elérhetőségét ellenőrzi</span><span class="sxs-lookup"><span data-stu-id="7326f-108">Example 1: Checks the availability of a container registry name</span></span>
```powershell
PS C:\>Test-AzContainerRegistryNameAvailability -Name 'SomeRegistryName'

NameAvailable Reason Message
------------- ------ -------
         True
```

<span data-ttu-id="7326f-109">Ez a parancs ellenőrzi, hogy rendelkezésre áll-e a \` SomeRegistryName nevű \` tárolóadatbázisnév.</span><span class="sxs-lookup"><span data-stu-id="7326f-109">This command checks the availability of the container registry name \`SomeRegistryName\`.</span></span>

## <span data-ttu-id="7326f-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7326f-110">PARAMETERS</span></span>

### <span data-ttu-id="7326f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7326f-111">-DefaultProfile</span></span>
<span data-ttu-id="7326f-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="7326f-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7326f-113">-Name</span><span class="sxs-lookup"><span data-stu-id="7326f-113">-Name</span></span>
<span data-ttu-id="7326f-114">Tároló beállításjegyzékének neve.</span><span class="sxs-lookup"><span data-stu-id="7326f-114">Container Registry Name.</span></span>

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

### <span data-ttu-id="7326f-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7326f-115">CommonParameters</span></span>
<span data-ttu-id="7326f-116">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7326f-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7326f-117">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7326f-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7326f-118">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7326f-118">INPUTS</span></span>

### <span data-ttu-id="7326f-119">System.String</span><span class="sxs-lookup"><span data-stu-id="7326f-119">System.String</span></span>

## <span data-ttu-id="7326f-120">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7326f-120">OUTPUTS</span></span>

### <span data-ttu-id="7326f-121">Microsoft.Azure.Management.ContainerRegistry.Models.RegistryNameStatus</span><span class="sxs-lookup"><span data-stu-id="7326f-121">Microsoft.Azure.Management.ContainerRegistry.Models.RegistryNameStatus</span></span>

## <span data-ttu-id="7326f-122">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="7326f-122">NOTES</span></span>

## <span data-ttu-id="7326f-123">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7326f-123">RELATED LINKS</span></span>

[<span data-ttu-id="7326f-124">New-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="7326f-124">New-AzContainerRegistry</span></span>]()

