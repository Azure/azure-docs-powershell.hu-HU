---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PowerBIEmbedded.dll-Help.xml
Module Name: Az.PowerBIEmbedded
ms.assetid: 3FED0088-47DA-4565-B9F0-DACF9B2DC0C7
online version: https://docs.microsoft.com/en-us/powershell/module/az.powerbiembedded/get-azpowerbiworkspacecollectionaccesskey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Get-AzPowerBIWorkspaceCollectionAccessKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Get-AzPowerBIWorkspaceCollectionAccessKey.md
ms.openlocfilehash: b9b6092035d97aed8f70137c4157bfb80bf3f62a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93669811"
---
# <span data-ttu-id="4833c-101">Get-AzPowerBIWorkspaceCollectionAccessKey</span><span class="sxs-lookup"><span data-stu-id="4833c-101">Get-AzPowerBIWorkspaceCollectionAccessKey</span></span>

## <span data-ttu-id="4833c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="4833c-102">SYNOPSIS</span></span>
<span data-ttu-id="4833c-103">A Power BI-munkaterületi gyűjteményhez társított jelenlegi hozzáférési kulcsokat kapja meg.</span><span class="sxs-lookup"><span data-stu-id="4833c-103">Gets the current access keys associated with a Power BI workspace collection.</span></span>

## <span data-ttu-id="4833c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="4833c-104">SYNTAX</span></span>

```
Get-AzPowerBIWorkspaceCollectionAccessKey [-ResourceGroupName] <String> [-WorkspaceCollectionName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4833c-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="4833c-105">DESCRIPTION</span></span>
<span data-ttu-id="4833c-106">A **Get-AzPowerBIWorkspaceCollectionAccessKey** parancsmag a Power bi-munkaterületi gyűjteményhez társított jelenlegi hozzáférési kulcsokat kapja meg.</span><span class="sxs-lookup"><span data-stu-id="4833c-106">The **Get-AzPowerBIWorkspaceCollectionAccessKey** cmdlet gets the current access keys associated with a Power BI workspace collection.</span></span>

## <span data-ttu-id="4833c-107">Példák</span><span class="sxs-lookup"><span data-stu-id="4833c-107">EXAMPLES</span></span>

### <span data-ttu-id="4833c-108">1. példa: a hozzáférési kulcsok beolvasása</span><span class="sxs-lookup"><span data-stu-id="4833c-108">Example 1: Get access keys</span></span>
```
PS C:\>Get-AzPowerBIWorkspaceCollectionAccessKey -ResourceGroupName "ResourceGroup17" -WorkspaceCollectionName "WCN11"
```

<span data-ttu-id="4833c-109">Ez a parancs a megadott erőforráscsoport WCN11 nevű munkaterületi gyűjteményhez hozzáférő kulcsokat kap.</span><span class="sxs-lookup"><span data-stu-id="4833c-109">This command gets access keys for the workspace collection named WCN11 in the specified resource group.</span></span>

## <span data-ttu-id="4833c-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="4833c-110">PARAMETERS</span></span>

### <span data-ttu-id="4833c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4833c-111">-DefaultProfile</span></span>
<span data-ttu-id="4833c-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="4833c-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4833c-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4833c-113">-ResourceGroupName</span></span>
<span data-ttu-id="4833c-114">A gyűjtemény erőforráscsoport-csoportjának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="4833c-114">Specifies the name of the resource group of the collection.</span></span>

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

### <span data-ttu-id="4833c-115">-WorkspaceCollectionName</span><span class="sxs-lookup"><span data-stu-id="4833c-115">-WorkspaceCollectionName</span></span>
<span data-ttu-id="4833c-116">Annak a Power BI-munkaterületi gyűjteménynek a nevét adja meg, amelyen a parancsmag működik.</span><span class="sxs-lookup"><span data-stu-id="4833c-116">Specifies the name of the Power BI workspace collection on which this cmdlet operates.</span></span>

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

### <span data-ttu-id="4833c-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4833c-117">CommonParameters</span></span>
<span data-ttu-id="4833c-118">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="4833c-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4833c-119">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4833c-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4833c-120">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="4833c-120">INPUTS</span></span>

### <span data-ttu-id="4833c-121">System. String</span><span class="sxs-lookup"><span data-stu-id="4833c-121">System.String</span></span>

## <span data-ttu-id="4833c-122">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4833c-122">OUTPUTS</span></span>

### <span data-ttu-id="4833c-123">Microsoft. Azure. Command. Management. PowerBIEmbedded. models. PSWorkspaceCollectionAccessKey</span><span class="sxs-lookup"><span data-stu-id="4833c-123">Microsoft.Azure.Commands.Management.PowerBIEmbedded.Models.PSWorkspaceCollectionAccessKey</span></span>

## <span data-ttu-id="4833c-124">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="4833c-124">NOTES</span></span>

## <span data-ttu-id="4833c-125">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4833c-125">RELATED LINKS</span></span>

[<span data-ttu-id="4833c-126">Reset-AzPowerBIWorkspaceCollectionAccessKey</span><span class="sxs-lookup"><span data-stu-id="4833c-126">Reset-AzPowerBIWorkspaceCollectionAccessKey</span></span>](./Reset-AzPowerBIWorkspaceCollectionAccessKey.md)


