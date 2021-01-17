---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AnalysisServices.dll-Help.xml
Module Name: Az.AnalysisServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.analysisservices/test-azanalysisservicesserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Test-AzAnalysisServicesServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Test-AzAnalysisServicesServer.md
ms.openlocfilehash: 86a82d5c82cdb775e7b07c6189244e494d14c4a8
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98479062"
---
# <span data-ttu-id="20ecd-101">Test-AzAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="20ecd-101">Test-AzAnalysisServicesServer</span></span>

## <span data-ttu-id="20ecd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="20ecd-102">SYNOPSIS</span></span>
<span data-ttu-id="20ecd-103">Annak vizsgálata, hogy az Analysis Services-kiszolgáló példánya létezik-e</span><span class="sxs-lookup"><span data-stu-id="20ecd-103">Tests the existence of an instance of Analysis Services server</span></span>

## <span data-ttu-id="20ecd-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="20ecd-104">SYNTAX</span></span>

```
Test-AzAnalysisServicesServer [-Name] <String> [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="20ecd-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="20ecd-105">DESCRIPTION</span></span>
<span data-ttu-id="20ecd-106">A Test-AzAnalysisServicesServer parancsmag teszteli az Analysis Services-kiszolgáló egy példányának meglétét</span><span class="sxs-lookup"><span data-stu-id="20ecd-106">The Test-AzAnalysisServicesServer cmdlet tests the existence of an instance of Analysis Services server</span></span>

## <span data-ttu-id="20ecd-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="20ecd-107">EXAMPLES</span></span>

### <span data-ttu-id="20ecd-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="20ecd-108">Example 1</span></span>
```
PS C:\> Test-AzAnalysisServicesServer -Name "testserver" -ResourceGroupName "testgroup"
```

<span data-ttu-id="20ecd-109">Ez a parancs teszteli, hogy van-e testserver nevű kiszolgáló az erőforráscsoport tesztcsoportban</span><span class="sxs-lookup"><span data-stu-id="20ecd-109">This command will test if there is a server named testserver in the resourcegroup testgroup</span></span>

## <span data-ttu-id="20ecd-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="20ecd-110">PARAMETERS</span></span>

### <span data-ttu-id="20ecd-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="20ecd-111">-DefaultProfile</span></span>
<span data-ttu-id="20ecd-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="20ecd-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="20ecd-113">-Name</span><span class="sxs-lookup"><span data-stu-id="20ecd-113">-Name</span></span>
<span data-ttu-id="20ecd-114">Az Analysis Services-kiszolgáló neve</span><span class="sxs-lookup"><span data-stu-id="20ecd-114">Name of the Analysis Services server</span></span>

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

### <span data-ttu-id="20ecd-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="20ecd-115">-ResourceGroupName</span></span>
<span data-ttu-id="20ecd-116">Annak az Azure-erőforráscsoportnak a neve, amelyhez a kiszolgáló tartozik</span><span class="sxs-lookup"><span data-stu-id="20ecd-116">Name of the Azure resource group to which the server belongs</span></span>

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

### <span data-ttu-id="20ecd-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="20ecd-117">CommonParameters</span></span>
<span data-ttu-id="20ecd-118">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="20ecd-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="20ecd-119">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="20ecd-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="20ecd-120">INPUTS</span><span class="sxs-lookup"><span data-stu-id="20ecd-120">INPUTS</span></span>

### <span data-ttu-id="20ecd-121">System.String</span><span class="sxs-lookup"><span data-stu-id="20ecd-121">System.String</span></span>

## <span data-ttu-id="20ecd-122">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="20ecd-122">OUTPUTS</span></span>

### <span data-ttu-id="20ecd-123">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="20ecd-123">System.Boolean</span></span>

## <span data-ttu-id="20ecd-124">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="20ecd-124">NOTES</span></span>
<span data-ttu-id="20ecd-125">Alias: Test-AzAs</span><span class="sxs-lookup"><span data-stu-id="20ecd-125">Alias: Test-AzAs</span></span>

## <span data-ttu-id="20ecd-126">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="20ecd-126">RELATED LINKS</span></span>

[<span data-ttu-id="20ecd-127">Get-AzAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="20ecd-127">Get-AzAnalysisServicesServer</span></span>](./Get-AzAnalysisServicesServer.md)

[<span data-ttu-id="20ecd-128">Remove-AzAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="20ecd-128">Remove-AzAnalysisServicesServer</span></span>](./Remove-AzAnalysisServicesServer.md)
