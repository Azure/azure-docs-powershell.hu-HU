---
external help file: Microsoft.Azure.Commands.Management.PowerBIEmbedded.dll-Help.xml
Module Name: AzureRM.PowerBIEmbedded
ms.assetid: 3FED0088-47DA-4565-B9F0-DACF9B2DC0C7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.powerbiembedded/get-azurermpowerbiworkspacecollectionaccesskeys
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.Management.PowerBIEmbedded/help/Get-AzureRmPowerBIWorkspaceCollectionAccessKeys.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.Management.PowerBIEmbedded/help/Get-AzureRmPowerBIWorkspaceCollectionAccessKeys.md
ms.openlocfilehash: 11c1e3c19a6f5767fcfe1120cfa3561a73885f5c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93493699"
---
# <span data-ttu-id="3925b-101">Get-AzureRmPowerBIWorkspaceCollectionAccessKeys</span><span class="sxs-lookup"><span data-stu-id="3925b-101">Get-AzureRmPowerBIWorkspaceCollectionAccessKeys</span></span>

## <span data-ttu-id="3925b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="3925b-102">SYNOPSIS</span></span>
<span data-ttu-id="3925b-103">A Power BI-munkaterületi gyűjteményhez társított jelenlegi hozzáférési kulcsokat kapja meg.</span><span class="sxs-lookup"><span data-stu-id="3925b-103">Gets the current access keys associated with a Power BI workspace collection.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3925b-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="3925b-104">SYNTAX</span></span>

```
Get-AzureRmPowerBIWorkspaceCollectionAccessKeys [-ResourceGroupName] <String>
 [-WorkspaceCollectionName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3925b-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="3925b-105">DESCRIPTION</span></span>
<span data-ttu-id="3925b-106">A **Get-AzureRmPowerBIWorkspaceCollectionAccessKeys** parancsmag a Power bi-munkaterületi gyűjteményhez társított jelenlegi hozzáférési kulcsokat kapja meg.</span><span class="sxs-lookup"><span data-stu-id="3925b-106">The **Get-AzureRmPowerBIWorkspaceCollectionAccessKeys** cmdlet gets the current access keys associated with a Power BI workspace collection.</span></span>

## <span data-ttu-id="3925b-107">Példák</span><span class="sxs-lookup"><span data-stu-id="3925b-107">EXAMPLES</span></span>

### <span data-ttu-id="3925b-108">1. példa: a hozzáférési kulcsok beolvasása</span><span class="sxs-lookup"><span data-stu-id="3925b-108">Example 1: Get access keys</span></span>
```
PS C:\>Get-AzureRmPowerBIWorkspaceCollectionAccessKeys -ResourceGroupName "ResourceGroup17" -WorkspaceCollectionName "WCN11"
```

<span data-ttu-id="3925b-109">Ez a parancs a megadott erőforráscsoport WCN11 nevű munkaterületi gyűjteményhez hozzáférő kulcsokat kap.</span><span class="sxs-lookup"><span data-stu-id="3925b-109">This command gets access keys for the workspace collection named WCN11 in the specified resource group.</span></span>

## <span data-ttu-id="3925b-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="3925b-110">PARAMETERS</span></span>

### <span data-ttu-id="3925b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3925b-111">-DefaultProfile</span></span>
<span data-ttu-id="3925b-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="3925b-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3925b-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3925b-113">-ResourceGroupName</span></span>
<span data-ttu-id="3925b-114">A gyűjtemény erőforráscsoport-csoportjának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="3925b-114">Specifies the name of the resource group of the collection.</span></span>

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

### <span data-ttu-id="3925b-115">-WorkspaceCollectionName</span><span class="sxs-lookup"><span data-stu-id="3925b-115">-WorkspaceCollectionName</span></span>
<span data-ttu-id="3925b-116">Annak a Power BI-munkaterületi gyűjteménynek a nevét adja meg, amelyen a parancsmag működik.</span><span class="sxs-lookup"><span data-stu-id="3925b-116">Specifies the name of the Power BI workspace collection on which this cmdlet operates.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name, ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3925b-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3925b-117">CommonParameters</span></span>
<span data-ttu-id="3925b-118">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="3925b-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3925b-119">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3925b-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3925b-120">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="3925b-120">INPUTS</span></span>

### <span data-ttu-id="3925b-121">Nincs</span><span class="sxs-lookup"><span data-stu-id="3925b-121">None</span></span>
<span data-ttu-id="3925b-122">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="3925b-122">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="3925b-123">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3925b-123">OUTPUTS</span></span>

### <span data-ttu-id="3925b-124">Microsoft. Azure. Command. Management. PowerBIEmbedded. models. PSWorkspaceCollectionAccessKey</span><span class="sxs-lookup"><span data-stu-id="3925b-124">Microsoft.Azure.Commands.Management.PowerBIEmbedded.Models.PSWorkspaceCollectionAccessKey</span></span>

## <span data-ttu-id="3925b-125">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="3925b-125">NOTES</span></span>

## <span data-ttu-id="3925b-126">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3925b-126">RELATED LINKS</span></span>

[<span data-ttu-id="3925b-127">Reset-AzureRmPowerBIWorkspaceCollectionAccessKeys</span><span class="sxs-lookup"><span data-stu-id="3925b-127">Reset-AzureRmPowerBIWorkspaceCollectionAccessKeys</span></span>](./Reset-AzureRmPowerBIWorkspaceCollectionAccessKeys.md)


