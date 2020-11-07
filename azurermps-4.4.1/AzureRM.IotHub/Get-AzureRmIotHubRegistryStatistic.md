---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Get-AzureRmIotHubRegistryStatistic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Get-AzureRmIotHubRegistryStatistic.md
ms.openlocfilehash: 033a7be2da102274837c881337fcb8f5bca4b879
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93679075"
---
# <span data-ttu-id="5433c-101">Get-AzureRmIotHubRegistryStatistic</span><span class="sxs-lookup"><span data-stu-id="5433c-101">Get-AzureRmIotHubRegistryStatistic</span></span>

## <span data-ttu-id="5433c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="5433c-102">SYNOPSIS</span></span>
<span data-ttu-id="5433c-103">Megkapja a RegistryStatistics egy IotHub.</span><span class="sxs-lookup"><span data-stu-id="5433c-103">Gets the RegistryStatistics for an IotHub.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5433c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="5433c-104">SYNTAX</span></span>

```
Get-AzureRmIotHubRegistryStatistic [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5433c-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="5433c-105">DESCRIPTION</span></span>
<span data-ttu-id="5433c-106">Megkapja a RegistryStatistics egy IotHub.</span><span class="sxs-lookup"><span data-stu-id="5433c-106">Gets the RegistryStatistics for an IotHub.</span></span>
<span data-ttu-id="5433c-107">Ez a cikk tájékoztatást nyújt arról, hogy hány teljes, engedélyezett és letiltott eszköz van egy IotHub.</span><span class="sxs-lookup"><span data-stu-id="5433c-107">This provides information about the number of total, enabled and disabled devices in an IotHub.</span></span>

## <span data-ttu-id="5433c-108">Példák</span><span class="sxs-lookup"><span data-stu-id="5433c-108">EXAMPLES</span></span>

### <span data-ttu-id="5433c-109">Példa 1 a RegistryStatistics beszerzése</span><span class="sxs-lookup"><span data-stu-id="5433c-109">Example 1 Get the RegistryStatistics</span></span>
```
PS C:\> Get-AzureRmIotHubRegistryStatistic -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="5433c-110">A "myiothub" nevű IotHub RegistryStatictics kapja.</span><span class="sxs-lookup"><span data-stu-id="5433c-110">Gets the RegistryStatictics for the IotHub named "myiothub"</span></span>

## <span data-ttu-id="5433c-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="5433c-111">PARAMETERS</span></span>

### <span data-ttu-id="5433c-112">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="5433c-112">-Name</span></span>
<span data-ttu-id="5433c-113">A IoT-központ neve.</span><span class="sxs-lookup"><span data-stu-id="5433c-113">Name of the IoT hub.</span></span> 

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5433c-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5433c-114">-ResourceGroupName</span></span>
<span data-ttu-id="5433c-115">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="5433c-115">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5433c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5433c-116">-DefaultProfile</span></span>
<span data-ttu-id="5433c-117">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="5433c-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5433c-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5433c-118">CommonParameters</span></span>
<span data-ttu-id="5433c-119">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="5433c-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5433c-120">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5433c-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5433c-121">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="5433c-121">INPUTS</span></span>

### <span data-ttu-id="5433c-122">System. String</span><span class="sxs-lookup"><span data-stu-id="5433c-122">System.String</span></span>

## <span data-ttu-id="5433c-123">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5433c-123">OUTPUTS</span></span>

### <span data-ttu-id="5433c-124">System. Collections. Generic. IList ' 1 [[Microsoft. Azure. Command. Management. IotHub. models. PSIotHubRegistryStatistics, Microsoft. Azure. commands. IotHub, Version = 1.0.0.0, Culture = semleges, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="5433c-124">System.Collections.Generic.IList\`1[[Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubRegistryStatistics, Microsoft.Azure.Commands.IotHub, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="5433c-125">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="5433c-125">NOTES</span></span>

## <span data-ttu-id="5433c-126">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5433c-126">RELATED LINKS</span></span>

