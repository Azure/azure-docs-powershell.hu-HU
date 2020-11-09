---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 606C5453-F841-4574-95F8-5CC29A4186E1
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/get-azhdinsightproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightProperty.md
ms.openlocfilehash: e13b90da8e1901faf0b18eb6ebf3cc78ce1bbcda
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94296348"
---
# <span data-ttu-id="73946-101">Get-AzHDInsightProperty</span><span class="sxs-lookup"><span data-stu-id="73946-101">Get-AzHDInsightProperty</span></span>

## <span data-ttu-id="73946-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="73946-102">SYNOPSIS</span></span>
<span data-ttu-id="73946-103">Beolvassa a HDInsight szolgáltatás tulajdonságait, például a rendelkezésre álló helyeket és a kapacitást.</span><span class="sxs-lookup"><span data-stu-id="73946-103">Gets properties about the HDInsight service, such as available locations and capacity.</span></span>

## <span data-ttu-id="73946-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="73946-104">SYNTAX</span></span>

```
Get-AzHDInsightProperty [-Location] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="73946-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="73946-105">DESCRIPTION</span></span>
<span data-ttu-id="73946-106">A **Get-AzHDInsightProperty** parancsmag az Azure HDInsight-ra jellemző tulajdonságokat kapja meg, például az elérhető helyek listáját, a HDInsight, valamint a rendelkezésre álló számítási kapacitást.</span><span class="sxs-lookup"><span data-stu-id="73946-106">The **Get-AzHDInsightProperty** cmdlet gets properties specific to Azure HDInsight, such as the list of available locations, HDInsight cluster versions, and available compute capacity.</span></span>

## <span data-ttu-id="73946-107">Példák</span><span class="sxs-lookup"><span data-stu-id="73946-107">EXAMPLES</span></span>

### <span data-ttu-id="73946-108">Példa 1: az Azure HDInsight-fürtök tulajdonságainak beszerzése</span><span class="sxs-lookup"><span data-stu-id="73946-108">Example 1: Get the properties of an Azure HDInsight cluster</span></span>
```
PS C:\>Get-AzHDInsightProperty -Location "East US 2"
```

<span data-ttu-id="73946-109">Ez a parancs egy HDInsight-szolgáltatás tulajdonságainak beolvasása a kelet-amerikai (2) helyről.</span><span class="sxs-lookup"><span data-stu-id="73946-109">This command gets properties from an HDInsight service from location East US 2.</span></span>

## <span data-ttu-id="73946-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="73946-110">PARAMETERS</span></span>

### <span data-ttu-id="73946-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="73946-111">-DefaultProfile</span></span>
<span data-ttu-id="73946-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="73946-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="73946-113">-Hely</span><span class="sxs-lookup"><span data-stu-id="73946-113">-Location</span></span>
<span data-ttu-id="73946-114">Annak a helynek a helye, ahol a HDInsight tulajdonságait le szeretné olvasni.</span><span class="sxs-lookup"><span data-stu-id="73946-114">Specifies the location for which to fetch HDInsight properties.</span></span>

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

### <span data-ttu-id="73946-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="73946-115">CommonParameters</span></span>
<span data-ttu-id="73946-116">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="73946-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="73946-117">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="73946-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="73946-118">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="73946-118">INPUTS</span></span>

### <span data-ttu-id="73946-119">Nincs</span><span class="sxs-lookup"><span data-stu-id="73946-119">None</span></span>
## <span data-ttu-id="73946-120">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="73946-120">OUTPUTS</span></span>

### <span data-ttu-id="73946-121">Microsoft. Azure. Management. HDInsight. models. AzureHDInsightCapabilities</span><span class="sxs-lookup"><span data-stu-id="73946-121">Microsoft.Azure.Management.HDInsight.Models.AzureHDInsightCapabilities</span></span>
## <span data-ttu-id="73946-122">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="73946-122">NOTES</span></span>

## <span data-ttu-id="73946-123">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="73946-123">RELATED LINKS</span></span>
