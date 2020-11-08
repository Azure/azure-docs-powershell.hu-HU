---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/test-azcontainerregistrynameavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Test-AzContainerRegistryNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Test-AzContainerRegistryNameAvailability.md
ms.openlocfilehash: 153ed152c68444327f379fda9ab5009290cbc00a
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94181988"
---
# <span data-ttu-id="9d438-101">Test-AzContainerRegistryNameAvailability</span><span class="sxs-lookup"><span data-stu-id="9d438-101">Test-AzContainerRegistryNameAvailability</span></span>

## <span data-ttu-id="9d438-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="9d438-102">SYNOPSIS</span></span>
<span data-ttu-id="9d438-103">Ellenőrzi a tároló beállításjegyzék-nevének elérhetőségét.</span><span class="sxs-lookup"><span data-stu-id="9d438-103">Checks the availability of a container registry name.</span></span>

## <span data-ttu-id="9d438-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="9d438-104">SYNTAX</span></span>

```
Test-AzContainerRegistryNameAvailability [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9d438-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="9d438-105">DESCRIPTION</span></span>
<span data-ttu-id="9d438-106">Az Test-AzContainerRegistryNameAvailability parancsmag ellenőrzi, hogy érvényes-e a tárolók neve, és használható-e.</span><span class="sxs-lookup"><span data-stu-id="9d438-106">The Test-AzContainerRegistryNameAvailability cmdlet checks whether a container registry name is valid and available to use.</span></span>

## <span data-ttu-id="9d438-107">Példák</span><span class="sxs-lookup"><span data-stu-id="9d438-107">EXAMPLES</span></span>

### <span data-ttu-id="9d438-108">1. példa: a tároló rendszerleíró nevének elérhetőségének ellenőrzése</span><span class="sxs-lookup"><span data-stu-id="9d438-108">Example 1: Checks the availability of a container registry name</span></span>
```powershell
PS C:\>Test-AzContainerRegistryNameAvailability -Name 'SomeRegistryName'

NameAvailable Reason Message
------------- ------ -------
         True
```

<span data-ttu-id="9d438-109">Ez a parancs ellenőrzi a tároló beállításjegyzék-neve SomeRegistryName elérhetőségét \` \` .</span><span class="sxs-lookup"><span data-stu-id="9d438-109">This command checks the availability of the container registry name \`SomeRegistryName\`.</span></span>

## <span data-ttu-id="9d438-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="9d438-110">PARAMETERS</span></span>

### <span data-ttu-id="9d438-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9d438-111">-DefaultProfile</span></span>
<span data-ttu-id="9d438-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="9d438-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9d438-113">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="9d438-113">-Name</span></span>
<span data-ttu-id="9d438-114">A tároló beállításjegyzékének neve.</span><span class="sxs-lookup"><span data-stu-id="9d438-114">Container Registry Name.</span></span>

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

### <span data-ttu-id="9d438-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9d438-115">CommonParameters</span></span>
<span data-ttu-id="9d438-116">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="9d438-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9d438-117">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="9d438-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9d438-118">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="9d438-118">INPUTS</span></span>

### <span data-ttu-id="9d438-119">System. String</span><span class="sxs-lookup"><span data-stu-id="9d438-119">System.String</span></span>

## <span data-ttu-id="9d438-120">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9d438-120">OUTPUTS</span></span>

### <span data-ttu-id="9d438-121">Microsoft. Azure. Management. ContainerRegistry. models. RegistryNameStatus</span><span class="sxs-lookup"><span data-stu-id="9d438-121">Microsoft.Azure.Management.ContainerRegistry.Models.RegistryNameStatus</span></span>

## <span data-ttu-id="9d438-122">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="9d438-122">NOTES</span></span>

## <span data-ttu-id="9d438-123">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9d438-123">RELATED LINKS</span></span>

[<span data-ttu-id="9d438-124">Új – AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="9d438-124">New-AzContainerRegistry</span></span>]()

