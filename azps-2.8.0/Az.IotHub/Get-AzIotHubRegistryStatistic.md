---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubregistrystatistic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubRegistryStatistic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubRegistryStatistic.md
ms.openlocfilehash: d7e1802bba2653e6574dc6eaf46cf4e457774605
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93666268"
---
# <span data-ttu-id="a394b-101">Get-AzIotHubRegistryStatistic</span><span class="sxs-lookup"><span data-stu-id="a394b-101">Get-AzIotHubRegistryStatistic</span></span>

## <span data-ttu-id="a394b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a394b-102">SYNOPSIS</span></span>
<span data-ttu-id="a394b-103">Megkapja a RegistryStatistics egy IotHub.</span><span class="sxs-lookup"><span data-stu-id="a394b-103">Gets the RegistryStatistics for an IotHub.</span></span>

## <span data-ttu-id="a394b-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a394b-104">SYNTAX</span></span>

```
Get-AzIotHubRegistryStatistic [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a394b-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="a394b-105">DESCRIPTION</span></span>
<span data-ttu-id="a394b-106">Megkapja a RegistryStatistics egy IotHub.</span><span class="sxs-lookup"><span data-stu-id="a394b-106">Gets the RegistryStatistics for an IotHub.</span></span>
<span data-ttu-id="a394b-107">Ez a cikk tájékoztatást nyújt arról, hogy hány teljes, engedélyezett és letiltott eszköz van egy IotHub.</span><span class="sxs-lookup"><span data-stu-id="a394b-107">This provides information about the number of total, enabled and disabled devices in an IotHub.</span></span>

## <span data-ttu-id="a394b-108">Példák</span><span class="sxs-lookup"><span data-stu-id="a394b-108">EXAMPLES</span></span>

### <span data-ttu-id="a394b-109">Példa 1 a RegistryStatistics beszerzése</span><span class="sxs-lookup"><span data-stu-id="a394b-109">Example 1 Get the RegistryStatistics</span></span>
```
PS C:\> Get-AzIotHubRegistryStatistic -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="a394b-110">A "myiothub" nevű IotHub RegistryStatistics kapja.</span><span class="sxs-lookup"><span data-stu-id="a394b-110">Gets the RegistryStatistics for the IotHub named "myiothub"</span></span>

## <span data-ttu-id="a394b-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a394b-111">PARAMETERS</span></span>

### <span data-ttu-id="a394b-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a394b-112">-DefaultProfile</span></span>
<span data-ttu-id="a394b-113">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="a394b-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a394b-114">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="a394b-114">-Name</span></span>
<span data-ttu-id="a394b-115">A IoT-központ neve.</span><span class="sxs-lookup"><span data-stu-id="a394b-115">Name of the IoT hub.</span></span> 

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

### <span data-ttu-id="a394b-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a394b-116">-ResourceGroupName</span></span>
<span data-ttu-id="a394b-117">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="a394b-117">Resource Group Name</span></span>

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

### <span data-ttu-id="a394b-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a394b-118">CommonParameters</span></span>
<span data-ttu-id="a394b-119">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a394b-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a394b-120">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a394b-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a394b-121">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a394b-121">INPUTS</span></span>

### <span data-ttu-id="a394b-122">System. String</span><span class="sxs-lookup"><span data-stu-id="a394b-122">System.String</span></span>

## <span data-ttu-id="a394b-123">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a394b-123">OUTPUTS</span></span>

### <span data-ttu-id="a394b-124">Microsoft. Azure. Command. Management. IotHub. models. PSIotHubRegistryStatistics</span><span class="sxs-lookup"><span data-stu-id="a394b-124">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubRegistryStatistics</span></span>

## <span data-ttu-id="a394b-125">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a394b-125">NOTES</span></span>

## <span data-ttu-id="a394b-126">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a394b-126">RELATED LINKS</span></span>
