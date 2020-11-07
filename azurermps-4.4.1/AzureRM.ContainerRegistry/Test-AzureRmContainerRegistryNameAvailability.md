---
external help file: Microsoft.Azure.Commands.ContainerRegistry.dll-Help.xml
Module Name: AzureRM.ContainerRegistry
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Test-AzureRmContainerRegistryNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Test-AzureRmContainerRegistryNameAvailability.md
ms.openlocfilehash: ad2a97895f4876c008d1740e962bb3b746e67ec8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93680598"
---
# <span data-ttu-id="45141-101">Test-AzureRmContainerRegistryNameAvailability</span><span class="sxs-lookup"><span data-stu-id="45141-101">Test-AzureRmContainerRegistryNameAvailability</span></span>

## <span data-ttu-id="45141-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="45141-102">SYNOPSIS</span></span>
<span data-ttu-id="45141-103">Ellenőrzi a tároló beállításjegyzék-nevének elérhetőségét.</span><span class="sxs-lookup"><span data-stu-id="45141-103">Checks the availability of a container registry name.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="45141-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="45141-104">SYNTAX</span></span>

```
Test-AzureRmContainerRegistryNameAvailability [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="45141-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="45141-105">DESCRIPTION</span></span>
<span data-ttu-id="45141-106">A **AzureRmContainerRegistryNameAvailability-** parancsmag ellenőrzi, hogy érvényes-e a tárolók neve, és használható-e.</span><span class="sxs-lookup"><span data-stu-id="45141-106">The **Test-AzureRmContainerRegistryNameAvailability** cmdlet checks whether a container registry name is valid and available to use.</span></span>

## <span data-ttu-id="45141-107">Példák</span><span class="sxs-lookup"><span data-stu-id="45141-107">EXAMPLES</span></span>

### <span data-ttu-id="45141-108">1. példa: a tárolók rendszerleíró nevének elérhetőségének ellenőrzése</span><span class="sxs-lookup"><span data-stu-id="45141-108">Example 1: Check the availability of a container registry name</span></span>
```
PS C:\>Test-AzureRmContainerRegistryNameAvailability -Name 'SomeRegistryName'

NameAvailable Reason Message
------------- ------ -------
         True
```

<span data-ttu-id="45141-109">Ez a parancs ellenőrzi a tároló beállításjegyzék-nevének elérhetőségét `SomeRegistryName` .</span><span class="sxs-lookup"><span data-stu-id="45141-109">This command checks the availability of the container registry name `SomeRegistryName`.</span></span>

## <span data-ttu-id="45141-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="45141-110">PARAMETERS</span></span>

### <span data-ttu-id="45141-111">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="45141-111">-Name</span></span>
<span data-ttu-id="45141-112">A tároló beállításjegyzékének neve.</span><span class="sxs-lookup"><span data-stu-id="45141-112">Container Registry Name.</span></span>

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

### <span data-ttu-id="45141-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="45141-113">-DefaultProfile</span></span>
<span data-ttu-id="45141-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="45141-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="45141-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="45141-115">CommonParameters</span></span>
<span data-ttu-id="45141-116">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="45141-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="45141-117">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="45141-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="45141-118">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="45141-118">INPUTS</span></span>

## <span data-ttu-id="45141-119">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="45141-119">OUTPUTS</span></span>

### <span data-ttu-id="45141-120">Microsoft. Azure. Management. ContainerRegistry. models. RegistryNameStatus</span><span class="sxs-lookup"><span data-stu-id="45141-120">Microsoft.Azure.Management.ContainerRegistry.Models.RegistryNameStatus</span></span>

## <span data-ttu-id="45141-121">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="45141-121">NOTES</span></span>

## <span data-ttu-id="45141-122">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="45141-122">RELATED LINKS</span></span>

[<span data-ttu-id="45141-123">Új – AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="45141-123">New-AzureRmContainerRegistry</span></span>](./New-AzureRmContainerRegistry.md)

