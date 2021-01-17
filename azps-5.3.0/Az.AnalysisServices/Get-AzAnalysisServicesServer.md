---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AnalysisServices.dll-Help.xml
Module Name: Az.AnalysisServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.analysisservices/get-azanalysisservicesserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Get-AzAnalysisServicesServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Get-AzAnalysisServicesServer.md
ms.openlocfilehash: c0c308bfe9d2d5fad971f9df1a26b03710d5629c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98469073"
---
# <span data-ttu-id="75768-101">Get-AzAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="75768-101">Get-AzAnalysisServicesServer</span></span>

## <span data-ttu-id="75768-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="75768-102">SYNOPSIS</span></span>
<span data-ttu-id="75768-103">Az Analysis Services-kiszolgáló adatait tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="75768-103">Gets the details of an Analysis Services server.</span></span>

## <span data-ttu-id="75768-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="75768-104">SYNTAX</span></span>

```
Get-AzAnalysisServicesServer [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="75768-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="75768-105">DESCRIPTION</span></span>
<span data-ttu-id="75768-106">A Get-AzAnalysisServicesServer parancsmag az Analysis Services-kiszolgáló adatait kapja.</span><span class="sxs-lookup"><span data-stu-id="75768-106">The Get-AzAnalysisServicesServer cmdlet gets the details of an Analysis Services server.</span></span>

## <span data-ttu-id="75768-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="75768-107">EXAMPLES</span></span>

### <span data-ttu-id="75768-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="75768-108">Example 1</span></span>
```
PS C:\>Get-AzAnalysisServicesServer -ResourceGroupName "ResourceGroup03"
```

<span data-ttu-id="75768-109">Ez a parancs a ResourceGroup03 nevű erőforráscsoport összes Azure Analysis Services-kiszolgálóját lekérte.</span><span class="sxs-lookup"><span data-stu-id="75768-109">This command gets all Azure Analysis Services servers in the resource group named ResourceGroup03.</span></span>

### <span data-ttu-id="75768-110">2. példa: Kiszolgáló lekérte</span><span class="sxs-lookup"><span data-stu-id="75768-110">Example 2: Get a server</span></span>
```
PS C:\>Get-AzAnalysisServicesServer -ResourceGroupName "ResourceGroup03" -Name "testserver"
```

<span data-ttu-id="75768-111">Ez a parancs a testserver nevű Azure Analysis Services-kiszolgálót az ResourceGroup03 nevű erőforráscsoportba kapja.</span><span class="sxs-lookup"><span data-stu-id="75768-111">This command gets the Azure Analysis Services server named testserver in the resource group named ResourceGroup03.</span></span>

## <span data-ttu-id="75768-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="75768-112">PARAMETERS</span></span>

### <span data-ttu-id="75768-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="75768-113">-DefaultProfile</span></span>
<span data-ttu-id="75768-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="75768-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="75768-115">-Name</span><span class="sxs-lookup"><span data-stu-id="75768-115">-Name</span></span>
<span data-ttu-id="75768-116">Az Analysis Services-kiszolgáló neve</span><span class="sxs-lookup"><span data-stu-id="75768-116">Name of the Analysis Services server</span></span>

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

### <span data-ttu-id="75768-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="75768-117">-ResourceGroupName</span></span>
<span data-ttu-id="75768-118">Annak az Azure-erőforráscsoportnak a neve, amelyhez a kiszolgáló tartozik</span><span class="sxs-lookup"><span data-stu-id="75768-118">Name of the Azure resource group to which the server belongs</span></span>

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

### <span data-ttu-id="75768-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="75768-119">CommonParameters</span></span>
<span data-ttu-id="75768-120">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="75768-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="75768-121">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="75768-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="75768-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="75768-122">INPUTS</span></span>

### <span data-ttu-id="75768-123">System.String</span><span class="sxs-lookup"><span data-stu-id="75768-123">System.String</span></span>

## <span data-ttu-id="75768-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="75768-124">OUTPUTS</span></span>

### <span data-ttu-id="75768-125">Microsoft.Azure.Commands.AnalysisServices.Models.AzureAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="75768-125">Microsoft.Azure.Commands.AnalysisServices.Models.AzureAnalysisServicesServer</span></span>

## <span data-ttu-id="75768-126">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="75768-126">NOTES</span></span>
<span data-ttu-id="75768-127">Alias: Get-AzAs</span><span class="sxs-lookup"><span data-stu-id="75768-127">Alias: Get-AzAs</span></span>

## <span data-ttu-id="75768-128">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="75768-128">RELATED LINKS</span></span>

[<span data-ttu-id="75768-129">New-AzAnalysisServicesServer </span><span class="sxs-lookup"><span data-stu-id="75768-129">New-AzAnalysisServicesServer </span></span>](./New-AzAnalysisServicesServer .md)

[<span data-ttu-id="75768-130">Remove-AzAnalysisServicesServer </span><span class="sxs-lookup"><span data-stu-id="75768-130">Remove-AzAnalysisServicesServer </span></span>](./Remove-AzAnalysisServicesServer .md)
