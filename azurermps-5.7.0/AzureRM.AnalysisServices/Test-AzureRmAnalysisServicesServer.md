---
external help file: Microsoft.Azure.Commands.AnalysisServices.dll-Help.xml
Module Name: AzureRM.AnalysisServices
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.analysisservices/test-azurermanalysisservicesserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices/help/Test-AzureRmAnalysisServicesServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices/help/Test-AzureRmAnalysisServicesServer.md
ms.openlocfilehash: 9dd8a86d1e98268708d7b0a12448df109ee083f2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93504647"
---
# <span data-ttu-id="4bb43-101">Test-AzureRmAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="4bb43-101">Test-AzureRmAnalysisServicesServer</span></span>

## <span data-ttu-id="4bb43-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="4bb43-102">SYNOPSIS</span></span>
<span data-ttu-id="4bb43-103">Az Analysis Services-kiszolgáló egy példányának tesztelése</span><span class="sxs-lookup"><span data-stu-id="4bb43-103">Tests the existence of an instance of Analysis Services server</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4bb43-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="4bb43-104">SYNTAX</span></span>

```
Test-AzureRmAnalysisServicesServer [-Name] <String> [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4bb43-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="4bb43-105">DESCRIPTION</span></span>
<span data-ttu-id="4bb43-106">A Test-AzureRmAnalysisServicesServer parancsmag teszteli az Analysis Services-kiszolgáló egy példányának létezését</span><span class="sxs-lookup"><span data-stu-id="4bb43-106">The Test-AzureRmAnalysisServicesServer cmdlet tests the existence of an instance of Analysis Services server</span></span>

## <span data-ttu-id="4bb43-107">Példák</span><span class="sxs-lookup"><span data-stu-id="4bb43-107">EXAMPLES</span></span>

### <span data-ttu-id="4bb43-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="4bb43-108">Example 1</span></span>
```
PS C:\> Test-AzureRmAnalysisServicesServer -Name "testserver" -ResourceGroupName "testgroup"
```

<span data-ttu-id="4bb43-109">Ez a parancs azt ellenőrzi, hogy van-e TestServer nevű kiszolgáló a resourcegroup testgroup</span><span class="sxs-lookup"><span data-stu-id="4bb43-109">This command will test if there is a server named testserver in the resourcegroup testgroup</span></span>

## <span data-ttu-id="4bb43-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="4bb43-110">PARAMETERS</span></span>

### <span data-ttu-id="4bb43-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4bb43-111">-DefaultProfile</span></span>
<span data-ttu-id="4bb43-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="4bb43-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4bb43-113">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="4bb43-113">-Name</span></span>
<span data-ttu-id="4bb43-114">Az Analysis Services-kiszolgáló neve</span><span class="sxs-lookup"><span data-stu-id="4bb43-114">Name of the Analysis Services server</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4bb43-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4bb43-115">-ResourceGroupName</span></span>
<span data-ttu-id="4bb43-116">Annak az Azure-erőforrás-csoportnak a neve, amelyhez a kiszolgáló tartozik</span><span class="sxs-lookup"><span data-stu-id="4bb43-116">Name of the Azure resource group to which the server belongs</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4bb43-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4bb43-117">CommonParameters</span></span>
<span data-ttu-id="4bb43-118">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="4bb43-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4bb43-119">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4bb43-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4bb43-120">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="4bb43-120">INPUTS</span></span>

### <span data-ttu-id="4bb43-121">Nincs</span><span class="sxs-lookup"><span data-stu-id="4bb43-121">None</span></span>
<span data-ttu-id="4bb43-122">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="4bb43-122">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="4bb43-123">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4bb43-123">OUTPUTS</span></span>

### <span data-ttu-id="4bb43-124">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="4bb43-124">System.Boolean</span></span>

## <span data-ttu-id="4bb43-125">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="4bb43-125">NOTES</span></span>
<span data-ttu-id="4bb43-126">Alias: Test-AzureAs</span><span class="sxs-lookup"><span data-stu-id="4bb43-126">Alias: Test-AzureAs</span></span>

## <span data-ttu-id="4bb43-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4bb43-127">RELATED LINKS</span></span>

[<span data-ttu-id="4bb43-128">Get-AzureRmAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="4bb43-128">Get-AzureRmAnalysisServicesServer</span></span>](./Get-AzureRmAnalysisServicesServer.md)

[<span data-ttu-id="4bb43-129">Remove-AzureRmAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="4bb43-129">Remove-AzureRmAnalysisServicesServer</span></span>](./Remove-AzureRmAnalysisServicesServer.md)