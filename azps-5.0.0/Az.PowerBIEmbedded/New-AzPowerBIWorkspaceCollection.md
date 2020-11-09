---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PowerBIEmbedded.dll-Help.xml
Module Name: Az.PowerBIEmbedded
ms.assetid: 9F9E4273-6747-4963-AF1F-C0AEB46770A4
online version: https://docs.microsoft.com/en-us/powershell/module/az.powerbiembedded/new-azpowerbiworkspacecollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/New-AzPowerBIWorkspaceCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/New-AzPowerBIWorkspaceCollection.md
ms.openlocfilehash: 557b1b7c5c2a91ec5e77729e70d2aa58f696d212
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94303410"
---
# <span data-ttu-id="e59de-101">New-AzPowerBIWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="e59de-101">New-AzPowerBIWorkspaceCollection</span></span>

## <span data-ttu-id="e59de-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e59de-102">SYNOPSIS</span></span>
<span data-ttu-id="e59de-103">Létrehoz egy Power BI-munkaterületi gyűjteményt.</span><span class="sxs-lookup"><span data-stu-id="e59de-103">Creates a Power BI workspace collection.</span></span>

## <span data-ttu-id="e59de-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e59de-104">SYNTAX</span></span>

```
New-AzPowerBIWorkspaceCollection [-ResourceGroupName] <String> [-WorkspaceCollectionName] <String>
 [-Location] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e59de-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="e59de-105">DESCRIPTION</span></span>
<span data-ttu-id="e59de-106">A **New-AzPowerBIWorkspaceCollection** parancsmag létrehoz egy Power bi-munkaterületi gyűjteményt az Azure-előfizetéshez a megadott erőforrás-csoportban és-helyen.</span><span class="sxs-lookup"><span data-stu-id="e59de-106">The **New-AzPowerBIWorkspaceCollection** cmdlet creates a Power BI workspace collection for your Azure subscription in the specified resource group and location.</span></span>

## <span data-ttu-id="e59de-107">Példák</span><span class="sxs-lookup"><span data-stu-id="e59de-107">EXAMPLES</span></span>

### <span data-ttu-id="e59de-108">Példa 1: munkaterületi gyűjtemény létrehozása</span><span class="sxs-lookup"><span data-stu-id="e59de-108">Example 1: Create a workspace collection</span></span>
```
PS C:\>New-AzPowerBIWorkspaceCollection -ResourceGroupName "ResourceGroup17" -WorkspaceCollectionName "WCN11" -Location "Japan West"
```

<span data-ttu-id="e59de-109">Ez a parancs létrehoz egy WCN11 nevű munkaterületi gyűjteményt a megadott helyen, a megadott erőforrás csoportban.</span><span class="sxs-lookup"><span data-stu-id="e59de-109">This command creates a workspace collection named WCN11 in the specified resource group in the specified location.</span></span>

## <span data-ttu-id="e59de-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e59de-110">PARAMETERS</span></span>

### <span data-ttu-id="e59de-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e59de-111">-DefaultProfile</span></span>
<span data-ttu-id="e59de-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="e59de-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e59de-113">-Hely</span><span class="sxs-lookup"><span data-stu-id="e59de-113">-Location</span></span>
<span data-ttu-id="e59de-114">Annak az Azure-helynek a meghatározása, amelyben ez a parancsmag létrehoz egy munkaterületi gyűjteményt.</span><span class="sxs-lookup"><span data-stu-id="e59de-114">Specifies the Azure location in which this cmdlet creates a workspace collection.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e59de-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e59de-115">-ResourceGroupName</span></span>
<span data-ttu-id="e59de-116">Annak az erőforrás csoportnak a nevét adja meg, amelyben a parancsmag létrehoz egy munkaterületi gyűjteményt.</span><span class="sxs-lookup"><span data-stu-id="e59de-116">Specifies the name of the resource group in which this cmdlet creates a workspace collection.</span></span>

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

### <span data-ttu-id="e59de-117">-WorkspaceCollectionName</span><span class="sxs-lookup"><span data-stu-id="e59de-117">-WorkspaceCollectionName</span></span>
<span data-ttu-id="e59de-118">A Power BI-munkaterületi gyűjtemény nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="e59de-118">Specifies a name for the Power BI workspace collection.</span></span>

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

### <span data-ttu-id="e59de-119">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="e59de-119">-Confirm</span></span>
<span data-ttu-id="e59de-120">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="e59de-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e59de-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e59de-121">-WhatIf</span></span>
<span data-ttu-id="e59de-122">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="e59de-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e59de-123">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="e59de-123">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e59de-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e59de-124">CommonParameters</span></span>
<span data-ttu-id="e59de-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e59de-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e59de-126">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e59de-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e59de-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e59de-127">INPUTS</span></span>

### <span data-ttu-id="e59de-128">System. String</span><span class="sxs-lookup"><span data-stu-id="e59de-128">System.String</span></span>

## <span data-ttu-id="e59de-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e59de-129">OUTPUTS</span></span>

### <span data-ttu-id="e59de-130">Microsoft. Azure. Command. Management. PowerBIEmbedded. models. PSWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="e59de-130">Microsoft.Azure.Commands.Management.PowerBIEmbedded.Models.PSWorkspaceCollection</span></span>

## <span data-ttu-id="e59de-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e59de-131">NOTES</span></span>

## <span data-ttu-id="e59de-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e59de-132">RELATED LINKS</span></span>

[<span data-ttu-id="e59de-133">Get-AzPowerBIWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="e59de-133">Get-AzPowerBIWorkspaceCollection</span></span>](./Get-AzPowerBIWorkspaceCollection.md)

[<span data-ttu-id="e59de-134">Remove-AzPowerBIWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="e59de-134">Remove-AzPowerBIWorkspaceCollection</span></span>](./Remove-AzPowerBIWorkspaceCollection.md)


