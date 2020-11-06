---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: 606C5453-F841-4574-95F8-5CC29A4186E1
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.hdinsight/get-azurermhdinsightproperties
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Get-AzureRmHDInsightProperties.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Get-AzureRmHDInsightProperties.md
ms.openlocfilehash: 198f0db3cab8b2e0f6e8f9b466ac3e0027e4638c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93496139"
---
# <span data-ttu-id="3cebd-101">Get-AzureRmHDInsightProperties</span><span class="sxs-lookup"><span data-stu-id="3cebd-101">Get-AzureRmHDInsightProperties</span></span>

## <span data-ttu-id="3cebd-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="3cebd-102">SYNOPSIS</span></span>
<span data-ttu-id="3cebd-103">Beolvassa a HDInsight szolgáltatás tulajdonságait, például a rendelkezésre álló helyeket és a kapacitást.</span><span class="sxs-lookup"><span data-stu-id="3cebd-103">Gets properties about the HDInsight service, such as available locations and capacity.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3cebd-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="3cebd-104">SYNTAX</span></span>

```
Get-AzureRmHDInsightProperties [-Location] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="3cebd-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="3cebd-105">DESCRIPTION</span></span>
<span data-ttu-id="3cebd-106">A **Get-AzureRmHDInsightProperties** parancsmag az Azure HDInsight-ra jellemző tulajdonságokat kapja meg, például az elérhető helyek listáját, a HDInsight, valamint a rendelkezésre álló számítási kapacitást.</span><span class="sxs-lookup"><span data-stu-id="3cebd-106">The **Get-AzureRmHDInsightProperties** cmdlet gets properties specific to Azure HDInsight, such as the list of available locations, HDInsight cluster versions, and available compute capacity.</span></span>

## <span data-ttu-id="3cebd-107">Példák</span><span class="sxs-lookup"><span data-stu-id="3cebd-107">EXAMPLES</span></span>

### <span data-ttu-id="3cebd-108">Példa 1: az Azure HDInsight-fürtök tulajdonságainak beszerzése</span><span class="sxs-lookup"><span data-stu-id="3cebd-108">Example 1: Get the properties of an Azure HDInsight cluster</span></span>
```
PS C:\>Get-AzureRmHDInsightProperties -Location "East US 2"
```

<span data-ttu-id="3cebd-109">Ez a parancs egy HDInsight-szolgáltatás tulajdonságainak beolvasása a kelet-amerikai (2) helyről.</span><span class="sxs-lookup"><span data-stu-id="3cebd-109">This command gets properties from an HDInsight service from location East US 2.</span></span>

## <span data-ttu-id="3cebd-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="3cebd-110">PARAMETERS</span></span>

### <span data-ttu-id="3cebd-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3cebd-111">-DefaultProfile</span></span>
<span data-ttu-id="3cebd-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="3cebd-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3cebd-113">-Hely</span><span class="sxs-lookup"><span data-stu-id="3cebd-113">-Location</span></span>
<span data-ttu-id="3cebd-114">Annak a helynek a helye, ahol a HDInsight tulajdonságait le szeretné olvasni.</span><span class="sxs-lookup"><span data-stu-id="3cebd-114">Specifies the location for which to fetch HDInsight properties.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3cebd-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3cebd-115">CommonParameters</span></span>
<span data-ttu-id="3cebd-116">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="3cebd-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3cebd-117">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3cebd-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3cebd-118">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="3cebd-118">INPUTS</span></span>

### <span data-ttu-id="3cebd-119">Nincs</span><span class="sxs-lookup"><span data-stu-id="3cebd-119">None</span></span>

## <span data-ttu-id="3cebd-120">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3cebd-120">OUTPUTS</span></span>

### <span data-ttu-id="3cebd-121">Microsoft. Azure. Management. HDInsight. models. CapabilitiesResponse</span><span class="sxs-lookup"><span data-stu-id="3cebd-121">Microsoft.Azure.Management.HDInsight.Models.CapabilitiesResponse</span></span>

## <span data-ttu-id="3cebd-122">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="3cebd-122">NOTES</span></span>

## <span data-ttu-id="3cebd-123">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3cebd-123">RELATED LINKS</span></span>
