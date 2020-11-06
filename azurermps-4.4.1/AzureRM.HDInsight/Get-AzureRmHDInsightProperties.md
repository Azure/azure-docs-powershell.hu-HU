---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: 606C5453-F841-4574-95F8-5CC29A4186E1
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Get-AzureRmHDInsightProperties.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Get-AzureRmHDInsightProperties.md
ms.openlocfilehash: e1701d60289343bb61a2891617fd10c6b9987b6d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93504995"
---
# <span data-ttu-id="27823-101">Get-AzureRmHDInsightProperties</span><span class="sxs-lookup"><span data-stu-id="27823-101">Get-AzureRmHDInsightProperties</span></span>

## <span data-ttu-id="27823-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="27823-102">SYNOPSIS</span></span>
<span data-ttu-id="27823-103">Beolvassa a HDInsight szolgáltatás tulajdonságait, például a rendelkezésre álló helyeket és a kapacitást.</span><span class="sxs-lookup"><span data-stu-id="27823-103">Gets properties about the HDInsight service, such as available locations and capacity.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="27823-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="27823-104">SYNTAX</span></span>

```
Get-AzureRmHDInsightProperties [-Location] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="27823-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="27823-105">DESCRIPTION</span></span>
<span data-ttu-id="27823-106">A **Get-AzureRmHDInsightProperties** parancsmag az Azure HDInsight-ra jellemző tulajdonságokat kapja meg, például az elérhető helyek listáját, a HDInsight, valamint a rendelkezésre álló számítási kapacitást.</span><span class="sxs-lookup"><span data-stu-id="27823-106">The **Get-AzureRmHDInsightProperties** cmdlet gets properties specific to Azure HDInsight, such as the list of available locations, HDInsight cluster versions, and available compute capacity.</span></span>

## <span data-ttu-id="27823-107">Példák</span><span class="sxs-lookup"><span data-stu-id="27823-107">EXAMPLES</span></span>

### <span data-ttu-id="27823-108">Példa 1: az Azure HDInsight-fürtök tulajdonságainak beszerzése</span><span class="sxs-lookup"><span data-stu-id="27823-108">Example 1: Get the properties of an Azure HDInsight cluster</span></span>
```
PS C:\>Get-AzureRmHDInsightProperties -Location "East US 2"
```

<span data-ttu-id="27823-109">Ez a parancs egy HDInsight-szolgáltatás tulajdonságainak beolvasása a kelet-amerikai (2) helyről.</span><span class="sxs-lookup"><span data-stu-id="27823-109">This command gets properties from an HDInsight service from location East US 2.</span></span>

## <span data-ttu-id="27823-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="27823-110">PARAMETERS</span></span>

### <span data-ttu-id="27823-111">-Hely</span><span class="sxs-lookup"><span data-stu-id="27823-111">-Location</span></span>
<span data-ttu-id="27823-112">Annak a helynek a helye, ahol a HDInsight tulajdonságait le szeretné olvasni.</span><span class="sxs-lookup"><span data-stu-id="27823-112">Specifies the location for which to fetch HDInsight properties.</span></span>

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

### <span data-ttu-id="27823-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="27823-113">-DefaultProfile</span></span>
<span data-ttu-id="27823-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="27823-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="27823-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="27823-115">CommonParameters</span></span>
<span data-ttu-id="27823-116">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="27823-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="27823-117">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="27823-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="27823-118">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="27823-118">INPUTS</span></span>

## <span data-ttu-id="27823-119">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="27823-119">OUTPUTS</span></span>

### <span data-ttu-id="27823-120">Microsoft. Azure. Management. HDInsight. models. CapabilitiesResponse</span><span class="sxs-lookup"><span data-stu-id="27823-120">Microsoft.Azure.Management.HDInsight.Models.CapabilitiesResponse</span></span>

## <span data-ttu-id="27823-121">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="27823-121">NOTES</span></span>

## <span data-ttu-id="27823-122">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="27823-122">RELATED LINKS</span></span>

