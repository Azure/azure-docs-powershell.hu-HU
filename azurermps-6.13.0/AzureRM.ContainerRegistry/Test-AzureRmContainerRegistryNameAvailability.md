---
external help file: Microsoft.Azure.Commands.ContainerRegistry.dll-Help.xml
Module Name: AzureRM.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.containerregistry/test-azurermcontainerregistrynameavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Test-AzureRmContainerRegistryNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Test-AzureRmContainerRegistryNameAvailability.md
ms.openlocfilehash: 996dfdb0c534369aed47787601f8a2883e2af788
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93494094"
---
# <span data-ttu-id="1e812-101">Test-AzureRmContainerRegistryNameAvailability</span><span class="sxs-lookup"><span data-stu-id="1e812-101">Test-AzureRmContainerRegistryNameAvailability</span></span>

## <span data-ttu-id="1e812-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="1e812-102">SYNOPSIS</span></span>
<span data-ttu-id="1e812-103">Ellenőrzi a tároló beállításjegyzék-nevének elérhetőségét.</span><span class="sxs-lookup"><span data-stu-id="1e812-103">Checks the availability of a container registry name.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1e812-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="1e812-104">SYNTAX</span></span>

```
Test-AzureRmContainerRegistryNameAvailability [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="1e812-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="1e812-105">DESCRIPTION</span></span>
<span data-ttu-id="1e812-106">Az Test-AzureRmContainerRegistryNameAvailability parancsmag ellenőrzi, hogy érvényes-e a tárolók neve, és használható-e.</span><span class="sxs-lookup"><span data-stu-id="1e812-106">The Test-AzureRmContainerRegistryNameAvailability cmdlet checks whether a container registry name is valid and available to use.</span></span>

## <span data-ttu-id="1e812-107">Példák</span><span class="sxs-lookup"><span data-stu-id="1e812-107">EXAMPLES</span></span>

### <span data-ttu-id="1e812-108">1. példa: a tároló rendszerleíró nevének elérhetőségének ellenőrzése</span><span class="sxs-lookup"><span data-stu-id="1e812-108">Example 1: Checks the availability of a container registry name</span></span>
```powershell
PS C:\>Test-AzureRmContainerRegistryNameAvailability -Name 'SomeRegistryName'

NameAvailable Reason Message
------------- ------ -------
         True
```

<span data-ttu-id="1e812-109">Ez a parancs ellenőrzi a tároló beállításjegyzék-neve SomeRegistryName elérhetőségét \` \` .</span><span class="sxs-lookup"><span data-stu-id="1e812-109">This command checks the availability of the container registry name \`SomeRegistryName\`.</span></span>

## <span data-ttu-id="1e812-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="1e812-110">PARAMETERS</span></span>

### <span data-ttu-id="1e812-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1e812-111">-DefaultProfile</span></span>
<span data-ttu-id="1e812-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="1e812-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1e812-113">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="1e812-113">-Name</span></span>
<span data-ttu-id="1e812-114">A tároló beállításjegyzékének neve.</span><span class="sxs-lookup"><span data-stu-id="1e812-114">Container Registry Name.</span></span>

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

### <span data-ttu-id="1e812-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1e812-115">CommonParameters</span></span>
<span data-ttu-id="1e812-116">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="1e812-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1e812-117">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1e812-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1e812-118">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="1e812-118">INPUTS</span></span>

### <span data-ttu-id="1e812-119">System. String</span><span class="sxs-lookup"><span data-stu-id="1e812-119">System.String</span></span>

## <span data-ttu-id="1e812-120">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1e812-120">OUTPUTS</span></span>

### <span data-ttu-id="1e812-121">Microsoft. Azure. Management. ContainerRegistry. models. RegistryNameStatus</span><span class="sxs-lookup"><span data-stu-id="1e812-121">Microsoft.Azure.Management.ContainerRegistry.Models.RegistryNameStatus</span></span>

## <span data-ttu-id="1e812-122">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="1e812-122">NOTES</span></span>

## <span data-ttu-id="1e812-123">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1e812-123">RELATED LINKS</span></span>

[<span data-ttu-id="1e812-124">Új – AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="1e812-124">New-AzureRmContainerRegistry</span></span>]()

