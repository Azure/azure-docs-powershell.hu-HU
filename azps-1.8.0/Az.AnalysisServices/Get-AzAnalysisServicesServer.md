---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AnalysisServices.dll-Help.xml
Module Name: Az.AnalysisServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.analysisservices/get-azanalysisservicesserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Get-AzAnalysisServicesServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Get-AzAnalysisServicesServer.md
ms.openlocfilehash: 6e5c8dccf2c6694511b21a05590415ab1a6bd126
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93665737"
---
# <span data-ttu-id="0e336-101">Get-AzAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="0e336-101">Get-AzAnalysisServicesServer</span></span>

## <span data-ttu-id="0e336-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="0e336-102">SYNOPSIS</span></span>
<span data-ttu-id="0e336-103">Az Analysis Services-kiszolgáló adatait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="0e336-103">Gets the details of an Analysis Services server.</span></span>

## <span data-ttu-id="0e336-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="0e336-104">SYNTAX</span></span>

```
Get-AzAnalysisServicesServer [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0e336-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="0e336-105">DESCRIPTION</span></span>
<span data-ttu-id="0e336-106">A Get-AzAnalysisServicesServer parancsmag az Analysis Services-kiszolgáló adatait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="0e336-106">The Get-AzAnalysisServicesServer cmdlet gets the details of an Analysis Services server.</span></span>

## <span data-ttu-id="0e336-107">Példák</span><span class="sxs-lookup"><span data-stu-id="0e336-107">EXAMPLES</span></span>

### <span data-ttu-id="0e336-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="0e336-108">Example 1</span></span>
```
PS C:\>Get-AzAnalysisServicesServer -ResourceGroupName "ResourceGroup03"
```

<span data-ttu-id="0e336-109">Ez a parancs a ResourceGroup03 nevű erőforráscsoport minden Azure Analysis Services-kiszolgálóját bekapja.</span><span class="sxs-lookup"><span data-stu-id="0e336-109">This command gets all Azure Analysis Services servers in the resource group named ResourceGroup03.</span></span>

### <span data-ttu-id="0e336-110">2. példa: kiszolgáló beszerzése</span><span class="sxs-lookup"><span data-stu-id="0e336-110">Example 2: Get a server</span></span>
```
PS C:\>Get-AzAnalysisServicesServer -ResourceGroupName "ResourceGroup03" -Name "testserver"
```

<span data-ttu-id="0e336-111">Ez a parancs a TestServer nevű Azure Analysis Services Servert kapja meg az ResourceGroup03 nevű erőforráscsoport nevű erőforrás-csoportban.</span><span class="sxs-lookup"><span data-stu-id="0e336-111">This command gets the Azure Analysis Services server named testserver in the resource group named ResourceGroup03.</span></span>

## <span data-ttu-id="0e336-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="0e336-112">PARAMETERS</span></span>

### <span data-ttu-id="0e336-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0e336-113">-DefaultProfile</span></span>
<span data-ttu-id="0e336-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="0e336-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0e336-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="0e336-115">-Name</span></span>
<span data-ttu-id="0e336-116">Az Analysis Services-kiszolgáló neve</span><span class="sxs-lookup"><span data-stu-id="0e336-116">Name of the Analysis Services server</span></span>

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

### <span data-ttu-id="0e336-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0e336-117">-ResourceGroupName</span></span>
<span data-ttu-id="0e336-118">Annak az Azure-erőforrás-csoportnak a neve, amelyhez a kiszolgáló tartozik</span><span class="sxs-lookup"><span data-stu-id="0e336-118">Name of the Azure resource group to which the server belongs</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0e336-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0e336-119">CommonParameters</span></span>
<span data-ttu-id="0e336-120">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="0e336-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0e336-121">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0e336-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0e336-122">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="0e336-122">INPUTS</span></span>

### <span data-ttu-id="0e336-123">System. String</span><span class="sxs-lookup"><span data-stu-id="0e336-123">System.String</span></span>

## <span data-ttu-id="0e336-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0e336-124">OUTPUTS</span></span>

### <span data-ttu-id="0e336-125">Microsoft. Azure. Command. AnalysisServices. models. AzureAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="0e336-125">Microsoft.Azure.Commands.AnalysisServices.Models.AzureAnalysisServicesServer</span></span>

## <span data-ttu-id="0e336-126">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="0e336-126">NOTES</span></span>
<span data-ttu-id="0e336-127">Alias: Get-AzAs</span><span class="sxs-lookup"><span data-stu-id="0e336-127">Alias: Get-AzAs</span></span>

## <span data-ttu-id="0e336-128">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0e336-128">RELATED LINKS</span></span>

[<span data-ttu-id="0e336-129">Új – AzAnalysisServicesServer </span><span class="sxs-lookup"><span data-stu-id="0e336-129">New-AzAnalysisServicesServer </span></span>](./New-AzAnalysisServicesServer .md)

[<span data-ttu-id="0e336-130">Remove-AzAnalysisServicesServer </span><span class="sxs-lookup"><span data-stu-id="0e336-130">Remove-AzAnalysisServicesServer </span></span>](./Remove-AzAnalysisServicesServer .md)
