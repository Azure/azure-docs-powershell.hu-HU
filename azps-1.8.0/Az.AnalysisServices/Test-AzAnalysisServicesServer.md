---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AnalysisServices.dll-Help.xml
Module Name: Az.AnalysisServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.analysisservices/test-azanalysisservicesserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Test-AzAnalysisServicesServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Test-AzAnalysisServicesServer.md
ms.openlocfilehash: 7298612cf64b4f90f65ebaa2943b38102b5ae1ff
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93665718"
---
# <span data-ttu-id="edc39-101">Test-AzAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="edc39-101">Test-AzAnalysisServicesServer</span></span>

## <span data-ttu-id="edc39-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="edc39-102">SYNOPSIS</span></span>
<span data-ttu-id="edc39-103">Az Analysis Services-kiszolgáló egy példányának tesztelése</span><span class="sxs-lookup"><span data-stu-id="edc39-103">Tests the existence of an instance of Analysis Services server</span></span>

## <span data-ttu-id="edc39-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="edc39-104">SYNTAX</span></span>

```
Test-AzAnalysisServicesServer [-Name] <String> [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="edc39-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="edc39-105">DESCRIPTION</span></span>
<span data-ttu-id="edc39-106">A Test-AzAnalysisServicesServer parancsmag teszteli az Analysis Services-kiszolgáló egy példányának létezését</span><span class="sxs-lookup"><span data-stu-id="edc39-106">The Test-AzAnalysisServicesServer cmdlet tests the existence of an instance of Analysis Services server</span></span>

## <span data-ttu-id="edc39-107">Példák</span><span class="sxs-lookup"><span data-stu-id="edc39-107">EXAMPLES</span></span>

### <span data-ttu-id="edc39-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="edc39-108">Example 1</span></span>
```
PS C:\> Test-AzAnalysisServicesServer -Name "testserver" -ResourceGroupName "testgroup"
```

<span data-ttu-id="edc39-109">Ez a parancs azt ellenőrzi, hogy van-e TestServer nevű kiszolgáló a resourcegroup testgroup</span><span class="sxs-lookup"><span data-stu-id="edc39-109">This command will test if there is a server named testserver in the resourcegroup testgroup</span></span>

## <span data-ttu-id="edc39-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="edc39-110">PARAMETERS</span></span>

### <span data-ttu-id="edc39-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="edc39-111">-DefaultProfile</span></span>
<span data-ttu-id="edc39-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="edc39-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="edc39-113">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="edc39-113">-Name</span></span>
<span data-ttu-id="edc39-114">Az Analysis Services-kiszolgáló neve</span><span class="sxs-lookup"><span data-stu-id="edc39-114">Name of the Analysis Services server</span></span>

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

### <span data-ttu-id="edc39-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="edc39-115">-ResourceGroupName</span></span>
<span data-ttu-id="edc39-116">Annak az Azure-erőforrás-csoportnak a neve, amelyhez a kiszolgáló tartozik</span><span class="sxs-lookup"><span data-stu-id="edc39-116">Name of the Azure resource group to which the server belongs</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="edc39-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="edc39-117">CommonParameters</span></span>
<span data-ttu-id="edc39-118">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="edc39-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="edc39-119">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="edc39-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="edc39-120">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="edc39-120">INPUTS</span></span>

### <span data-ttu-id="edc39-121">System. String</span><span class="sxs-lookup"><span data-stu-id="edc39-121">System.String</span></span>

## <span data-ttu-id="edc39-122">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="edc39-122">OUTPUTS</span></span>

### <span data-ttu-id="edc39-123">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="edc39-123">System.Boolean</span></span>

## <span data-ttu-id="edc39-124">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="edc39-124">NOTES</span></span>
<span data-ttu-id="edc39-125">Alias: Test-AzAs</span><span class="sxs-lookup"><span data-stu-id="edc39-125">Alias: Test-AzAs</span></span>

## <span data-ttu-id="edc39-126">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="edc39-126">RELATED LINKS</span></span>

[<span data-ttu-id="edc39-127">Get-AzAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="edc39-127">Get-AzAnalysisServicesServer</span></span>](./Get-AzAnalysisServicesServer.md)

[<span data-ttu-id="edc39-128">Remove-AzAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="edc39-128">Remove-AzAnalysisServicesServer</span></span>](./Remove-AzAnalysisServicesServer.md)
