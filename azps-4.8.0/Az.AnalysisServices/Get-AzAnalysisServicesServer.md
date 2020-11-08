---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AnalysisServices.dll-Help.xml
Module Name: Az.AnalysisServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.analysisservices/get-azanalysisservicesserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Get-AzAnalysisServicesServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Get-AzAnalysisServicesServer.md
ms.openlocfilehash: c0c308bfe9d2d5fad971f9df1a26b03710d5629c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94182677"
---
# <span data-ttu-id="dec29-101">Get-AzAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="dec29-101">Get-AzAnalysisServicesServer</span></span>

## <span data-ttu-id="dec29-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="dec29-102">SYNOPSIS</span></span>
<span data-ttu-id="dec29-103">Az Analysis Services-kiszolgáló adatait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="dec29-103">Gets the details of an Analysis Services server.</span></span>

## <span data-ttu-id="dec29-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="dec29-104">SYNTAX</span></span>

```
Get-AzAnalysisServicesServer [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dec29-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="dec29-105">DESCRIPTION</span></span>
<span data-ttu-id="dec29-106">A Get-AzAnalysisServicesServer parancsmag az Analysis Services-kiszolgáló adatait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="dec29-106">The Get-AzAnalysisServicesServer cmdlet gets the details of an Analysis Services server.</span></span>

## <span data-ttu-id="dec29-107">Példák</span><span class="sxs-lookup"><span data-stu-id="dec29-107">EXAMPLES</span></span>

### <span data-ttu-id="dec29-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="dec29-108">Example 1</span></span>
```
PS C:\>Get-AzAnalysisServicesServer -ResourceGroupName "ResourceGroup03"
```

<span data-ttu-id="dec29-109">Ez a parancs a ResourceGroup03 nevű erőforráscsoport minden Azure Analysis Services-kiszolgálóját bekapja.</span><span class="sxs-lookup"><span data-stu-id="dec29-109">This command gets all Azure Analysis Services servers in the resource group named ResourceGroup03.</span></span>

### <span data-ttu-id="dec29-110">2. példa: kiszolgáló beszerzése</span><span class="sxs-lookup"><span data-stu-id="dec29-110">Example 2: Get a server</span></span>
```
PS C:\>Get-AzAnalysisServicesServer -ResourceGroupName "ResourceGroup03" -Name "testserver"
```

<span data-ttu-id="dec29-111">Ez a parancs a TestServer nevű Azure Analysis Services Servert kapja meg az ResourceGroup03 nevű erőforráscsoport nevű erőforrás-csoportban.</span><span class="sxs-lookup"><span data-stu-id="dec29-111">This command gets the Azure Analysis Services server named testserver in the resource group named ResourceGroup03.</span></span>

## <span data-ttu-id="dec29-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="dec29-112">PARAMETERS</span></span>

### <span data-ttu-id="dec29-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dec29-113">-DefaultProfile</span></span>
<span data-ttu-id="dec29-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="dec29-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dec29-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="dec29-115">-Name</span></span>
<span data-ttu-id="dec29-116">Az Analysis Services-kiszolgáló neve</span><span class="sxs-lookup"><span data-stu-id="dec29-116">Name of the Analysis Services server</span></span>

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

### <span data-ttu-id="dec29-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dec29-117">-ResourceGroupName</span></span>
<span data-ttu-id="dec29-118">Annak az Azure-erőforrás-csoportnak a neve, amelyhez a kiszolgáló tartozik</span><span class="sxs-lookup"><span data-stu-id="dec29-118">Name of the Azure resource group to which the server belongs</span></span>

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

### <span data-ttu-id="dec29-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dec29-119">CommonParameters</span></span>
<span data-ttu-id="dec29-120">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="dec29-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dec29-121">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dec29-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dec29-122">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="dec29-122">INPUTS</span></span>

### <span data-ttu-id="dec29-123">System. String</span><span class="sxs-lookup"><span data-stu-id="dec29-123">System.String</span></span>

## <span data-ttu-id="dec29-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="dec29-124">OUTPUTS</span></span>

### <span data-ttu-id="dec29-125">Microsoft. Azure. Command. AnalysisServices. models. AzureAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="dec29-125">Microsoft.Azure.Commands.AnalysisServices.Models.AzureAnalysisServicesServer</span></span>

## <span data-ttu-id="dec29-126">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="dec29-126">NOTES</span></span>
<span data-ttu-id="dec29-127">Alias: Get-AzAs</span><span class="sxs-lookup"><span data-stu-id="dec29-127">Alias: Get-AzAs</span></span>

## <span data-ttu-id="dec29-128">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="dec29-128">RELATED LINKS</span></span>

[<span data-ttu-id="dec29-129">Új – AzAnalysisServicesServer </span><span class="sxs-lookup"><span data-stu-id="dec29-129">New-AzAnalysisServicesServer </span></span>](./New-AzAnalysisServicesServer .md)

[<span data-ttu-id="dec29-130">Remove-AzAnalysisServicesServer </span><span class="sxs-lookup"><span data-stu-id="dec29-130">Remove-AzAnalysisServicesServer </span></span>](./Remove-AzAnalysisServicesServer .md)
