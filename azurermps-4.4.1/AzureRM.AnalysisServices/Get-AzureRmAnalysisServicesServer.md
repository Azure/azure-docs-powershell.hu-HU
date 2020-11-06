---
external help file: Microsoft.Azure.Commands.AnalysisServices.dll-Help.xml
Module Name: AzureRM.AnalysisServices
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices/help/Get-AzureRmAnalysisServicesServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices/help/Get-AzureRmAnalysisServicesServer.md
ms.openlocfilehash: f80f3eead528c7731007bcd6611f5d6fecbb55e9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93493594"
---
# <span data-ttu-id="4c20b-101">Get-AzureRmAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="4c20b-101">Get-AzureRmAnalysisServicesServer</span></span>

## <span data-ttu-id="4c20b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="4c20b-102">SYNOPSIS</span></span>
<span data-ttu-id="4c20b-103">Az Analysis Services-kiszolgáló adatait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="4c20b-103">Gets the details of an Analysis Services server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4c20b-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="4c20b-104">SYNTAX</span></span>

```
Get-AzureRmAnalysisServicesServer [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4c20b-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="4c20b-105">DESCRIPTION</span></span>
<span data-ttu-id="4c20b-106">A Get-AzureRmAnalysisServicesServer parancsmag az Analysis Services-kiszolgáló adatait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="4c20b-106">The Get-AzureRmAnalysisServicesServer cmdlet gets the details of an Analysis Services server.</span></span>

## <span data-ttu-id="4c20b-107">Példák</span><span class="sxs-lookup"><span data-stu-id="4c20b-107">EXAMPLES</span></span>

### <span data-ttu-id="4c20b-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="4c20b-108">Example 1</span></span>
```
PS C:\>Get-AzureRmAnalysisServicesServer -ResourceGroupName "ResourceGroup03"
```

<span data-ttu-id="4c20b-109">Ez a parancs a ResourceGroup03 nevű erőforráscsoport minden Azure Analysis Services-kiszolgálóját bekapja.</span><span class="sxs-lookup"><span data-stu-id="4c20b-109">This command gets all Azure Analysis Services servers in the resource group named ResourceGroup03.</span></span>

### <span data-ttu-id="4c20b-110">2. példa: kiszolgáló beszerzése</span><span class="sxs-lookup"><span data-stu-id="4c20b-110">Example 2: Get a server</span></span>
```
PS C:\>Get-AzureRmAnalysisServicesServer -ResourceGroupName "ResourceGroup03" -Name "testserver"
```

<span data-ttu-id="4c20b-111">Ez a parancs a TestServer nevű Azure Analysis Services Servert kapja meg az ResourceGroup03 nevű erőforráscsoport nevű erőforrás-csoportban.</span><span class="sxs-lookup"><span data-stu-id="4c20b-111">This command gets the Azure Analysis Services server named testserver in the resource group named ResourceGroup03.</span></span>

## <span data-ttu-id="4c20b-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="4c20b-112">PARAMETERS</span></span>

### <span data-ttu-id="4c20b-113">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="4c20b-113">-Name</span></span>
<span data-ttu-id="4c20b-114">Az Analysis Services-kiszolgáló neve</span><span class="sxs-lookup"><span data-stu-id="4c20b-114">Name of the Analysis Services server</span></span>

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

### <span data-ttu-id="4c20b-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4c20b-115">-ResourceGroupName</span></span>
<span data-ttu-id="4c20b-116">Annak az Azure-erőforrás-csoportnak a neve, amelyhez a kiszolgáló tartozik</span><span class="sxs-lookup"><span data-stu-id="4c20b-116">Name of the Azure resource group to which the server belongs</span></span>

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

### <span data-ttu-id="4c20b-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4c20b-117">-DefaultProfile</span></span>
<span data-ttu-id="4c20b-118">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="4c20b-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4c20b-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4c20b-119">CommonParameters</span></span>
<span data-ttu-id="4c20b-120">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="4c20b-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4c20b-121">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4c20b-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4c20b-122">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="4c20b-122">INPUTS</span></span>

## <span data-ttu-id="4c20b-123">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4c20b-123">OUTPUTS</span></span>

### <span data-ttu-id="4c20b-124">Microsoft. Azure. Command. AnalysisServices. models. AzureAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="4c20b-124">Microsoft.Azure.Commands.AnalysisServices.Models.AzureAnalysisServicesServer</span></span>

## <span data-ttu-id="4c20b-125">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="4c20b-125">NOTES</span></span>
<span data-ttu-id="4c20b-126">Alias: Get-AzureAs</span><span class="sxs-lookup"><span data-stu-id="4c20b-126">Alias: Get-AzureAs</span></span>

## <span data-ttu-id="4c20b-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4c20b-127">RELATED LINKS</span></span>

[<span data-ttu-id="4c20b-128">Új – AzureRmAnalysisServicesServer </span><span class="sxs-lookup"><span data-stu-id="4c20b-128">New-AzureRmAnalysisServicesServer </span></span>](./New-AzureRmAnalysisServicesServer .md)

[<span data-ttu-id="4c20b-129">Remove-AzureRmAnalysisServicesServer </span><span class="sxs-lookup"><span data-stu-id="4c20b-129">Remove-AzureRmAnalysisServicesServer </span></span>](./Remove-AzureRmAnalysisServicesServer .md)
