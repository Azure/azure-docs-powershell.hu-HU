---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PowerBIEmbedded.dll-Help.xml
Module Name: Az.PowerBIEmbedded
ms.assetid: 3FED0088-47DA-4565-B9F0-DACF9B2DC0C7
online version: https://docs.microsoft.com/en-us/powershell/module/az.powerbiembedded/get-azpowerbiworkspacecollectionaccesskey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Get-AzPowerBIWorkspaceCollectionAccessKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Get-AzPowerBIWorkspaceCollectionAccessKey.md
ms.openlocfilehash: 9108f224297b23fd391e1a4c3afac4b826aa3dbf
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94025107"
---
# <span data-ttu-id="d77e3-101">Get-AzPowerBIWorkspaceCollectionAccessKey</span><span class="sxs-lookup"><span data-stu-id="d77e3-101">Get-AzPowerBIWorkspaceCollectionAccessKey</span></span>

## <span data-ttu-id="d77e3-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d77e3-102">SYNOPSIS</span></span>
<span data-ttu-id="d77e3-103">A Power BI-munkaterületi gyűjteményhez társított jelenlegi hozzáférési kulcsokat kapja meg.</span><span class="sxs-lookup"><span data-stu-id="d77e3-103">Gets the current access keys associated with a Power BI workspace collection.</span></span>

## <span data-ttu-id="d77e3-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d77e3-104">SYNTAX</span></span>

```
Get-AzPowerBIWorkspaceCollectionAccessKey [-ResourceGroupName] <String> [-WorkspaceCollectionName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d77e3-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="d77e3-105">DESCRIPTION</span></span>
<span data-ttu-id="d77e3-106">A **Get-AzPowerBIWorkspaceCollectionAccessKey** parancsmag a Power bi-munkaterületi gyűjteményhez társított jelenlegi hozzáférési kulcsokat kapja meg.</span><span class="sxs-lookup"><span data-stu-id="d77e3-106">The **Get-AzPowerBIWorkspaceCollectionAccessKey** cmdlet gets the current access keys associated with a Power BI workspace collection.</span></span>

## <span data-ttu-id="d77e3-107">Példák</span><span class="sxs-lookup"><span data-stu-id="d77e3-107">EXAMPLES</span></span>

### <span data-ttu-id="d77e3-108">1. példa: a hozzáférési kulcsok beolvasása</span><span class="sxs-lookup"><span data-stu-id="d77e3-108">Example 1: Get access keys</span></span>
```
PS C:\>Get-AzPowerBIWorkspaceCollectionAccessKey -ResourceGroupName "ResourceGroup17" -WorkspaceCollectionName "WCN11"
```

<span data-ttu-id="d77e3-109">Ez a parancs a megadott erőforráscsoport WCN11 nevű munkaterületi gyűjteményhez hozzáférő kulcsokat kap.</span><span class="sxs-lookup"><span data-stu-id="d77e3-109">This command gets access keys for the workspace collection named WCN11 in the specified resource group.</span></span>

## <span data-ttu-id="d77e3-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d77e3-110">PARAMETERS</span></span>

### <span data-ttu-id="d77e3-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d77e3-111">-DefaultProfile</span></span>
<span data-ttu-id="d77e3-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="d77e3-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d77e3-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d77e3-113">-ResourceGroupName</span></span>
<span data-ttu-id="d77e3-114">A gyűjtemény erőforráscsoport-csoportjának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="d77e3-114">Specifies the name of the resource group of the collection.</span></span>

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

### <span data-ttu-id="d77e3-115">-WorkspaceCollectionName</span><span class="sxs-lookup"><span data-stu-id="d77e3-115">-WorkspaceCollectionName</span></span>
<span data-ttu-id="d77e3-116">Annak a Power BI-munkaterületi gyűjteménynek a nevét adja meg, amelyen a parancsmag működik.</span><span class="sxs-lookup"><span data-stu-id="d77e3-116">Specifies the name of the Power BI workspace collection on which this cmdlet operates.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name, ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d77e3-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d77e3-117">CommonParameters</span></span>
<span data-ttu-id="d77e3-118">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d77e3-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d77e3-119">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d77e3-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d77e3-120">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d77e3-120">INPUTS</span></span>

### <span data-ttu-id="d77e3-121">System. String</span><span class="sxs-lookup"><span data-stu-id="d77e3-121">System.String</span></span>

## <span data-ttu-id="d77e3-122">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d77e3-122">OUTPUTS</span></span>

### <span data-ttu-id="d77e3-123">Microsoft. Azure. Command. Management. PowerBIEmbedded. models. PSWorkspaceCollectionAccessKey</span><span class="sxs-lookup"><span data-stu-id="d77e3-123">Microsoft.Azure.Commands.Management.PowerBIEmbedded.Models.PSWorkspaceCollectionAccessKey</span></span>

## <span data-ttu-id="d77e3-124">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d77e3-124">NOTES</span></span>

## <span data-ttu-id="d77e3-125">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d77e3-125">RELATED LINKS</span></span>

[<span data-ttu-id="d77e3-126">Reset-AzPowerBIWorkspaceCollectionAccessKey</span><span class="sxs-lookup"><span data-stu-id="d77e3-126">Reset-AzPowerBIWorkspaceCollectionAccessKey</span></span>](./Reset-AzPowerBIWorkspaceCollectionAccessKey.md)


