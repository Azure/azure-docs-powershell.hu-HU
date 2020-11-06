---
external help file: Microsoft.Azure.Commands.Management.PowerBIEmbedded.dll-Help.xml
Module Name: AzureRM.PowerBIEmbedded
ms.assetid: 9F9E4273-6747-4963-AF1F-C0AEB46770A4
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.powerbiembedded/new-azurermpowerbiworkspacecollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.Management.PowerBIEmbedded/help/New-AzureRmPowerBIWorkspaceCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.Management.PowerBIEmbedded/help/New-AzureRmPowerBIWorkspaceCollection.md
ms.openlocfilehash: 7ed4af8c6d5443c3cdc7c8ae395ecc66d0a927e6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93493991"
---
# <span data-ttu-id="b6f9d-101">New-AzureRmPowerBIWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="b6f9d-101">New-AzureRmPowerBIWorkspaceCollection</span></span>

## <span data-ttu-id="b6f9d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b6f9d-102">SYNOPSIS</span></span>
<span data-ttu-id="b6f9d-103">Létrehoz egy Power BI-munkaterületi gyűjteményt.</span><span class="sxs-lookup"><span data-stu-id="b6f9d-103">Creates a Power BI workspace collection.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b6f9d-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b6f9d-104">SYNTAX</span></span>

```
New-AzureRmPowerBIWorkspaceCollection [-ResourceGroupName] <String> [-WorkspaceCollectionName] <String>
 [-Location] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b6f9d-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="b6f9d-105">DESCRIPTION</span></span>
<span data-ttu-id="b6f9d-106">A **New-AzureRmPowerBIWorkspaceCollection** parancsmag létrehoz egy Power bi-munkaterületi gyűjteményt az Azure-előfizetéshez a megadott erőforrás-csoportban és-helyen.</span><span class="sxs-lookup"><span data-stu-id="b6f9d-106">The **New-AzureRmPowerBIWorkspaceCollection** cmdlet creates a Power BI workspace collection for your Azure subscription in the specified resource group and location.</span></span>

## <span data-ttu-id="b6f9d-107">Példák</span><span class="sxs-lookup"><span data-stu-id="b6f9d-107">EXAMPLES</span></span>

### <span data-ttu-id="b6f9d-108">Példa 1: munkaterületi gyűjtemény létrehozása</span><span class="sxs-lookup"><span data-stu-id="b6f9d-108">Example 1: Create a workspace collection</span></span>
```
PS C:\>New-AzureRmPowerBIWorkspaceCollection -ResourceGroupName "ResourceGroup17" -WorkspaceCollectionName "WCN11" -Location "Japan West"
```

<span data-ttu-id="b6f9d-109">Ez a parancs létrehoz egy WCN11 nevű munkaterületi gyűjteményt a megadott helyen, a megadott erőforrás csoportban.</span><span class="sxs-lookup"><span data-stu-id="b6f9d-109">This command creates a workspace collection named WCN11 in the specified resource group in the specified location.</span></span>

## <span data-ttu-id="b6f9d-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b6f9d-110">PARAMETERS</span></span>

### <span data-ttu-id="b6f9d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b6f9d-111">-DefaultProfile</span></span>
<span data-ttu-id="b6f9d-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="b6f9d-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b6f9d-113">-Hely</span><span class="sxs-lookup"><span data-stu-id="b6f9d-113">-Location</span></span>
<span data-ttu-id="b6f9d-114">Annak az Azure-helynek a meghatározása, amelyben ez a parancsmag létrehoz egy munkaterületi gyűjteményt.</span><span class="sxs-lookup"><span data-stu-id="b6f9d-114">Specifies the Azure location in which this cmdlet creates a workspace collection.</span></span>

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

### <span data-ttu-id="b6f9d-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b6f9d-115">-ResourceGroupName</span></span>
<span data-ttu-id="b6f9d-116">Annak az erőforrás csoportnak a nevét adja meg, amelyben a parancsmag létrehoz egy munkaterületi gyűjteményt.</span><span class="sxs-lookup"><span data-stu-id="b6f9d-116">Specifies the name of the resource group in which this cmdlet creates a workspace collection.</span></span>

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

### <span data-ttu-id="b6f9d-117">-WorkspaceCollectionName</span><span class="sxs-lookup"><span data-stu-id="b6f9d-117">-WorkspaceCollectionName</span></span>
<span data-ttu-id="b6f9d-118">A Power BI-munkaterületi gyűjtemény nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="b6f9d-118">Specifies a name for the Power BI workspace collection.</span></span>

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

### <span data-ttu-id="b6f9d-119">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="b6f9d-119">-Confirm</span></span>
<span data-ttu-id="b6f9d-120">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="b6f9d-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b6f9d-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b6f9d-121">-WhatIf</span></span>
<span data-ttu-id="b6f9d-122">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="b6f9d-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b6f9d-123">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="b6f9d-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b6f9d-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b6f9d-124">CommonParameters</span></span>
<span data-ttu-id="b6f9d-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b6f9d-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b6f9d-126">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b6f9d-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b6f9d-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b6f9d-127">INPUTS</span></span>

### <span data-ttu-id="b6f9d-128">System. String</span><span class="sxs-lookup"><span data-stu-id="b6f9d-128">System.String</span></span>

## <span data-ttu-id="b6f9d-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b6f9d-129">OUTPUTS</span></span>

### <span data-ttu-id="b6f9d-130">Microsoft. Azure. Command. Management. PowerBIEmbedded. models. PSWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="b6f9d-130">Microsoft.Azure.Commands.Management.PowerBIEmbedded.Models.PSWorkspaceCollection</span></span>

## <span data-ttu-id="b6f9d-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b6f9d-131">NOTES</span></span>

## <span data-ttu-id="b6f9d-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b6f9d-132">RELATED LINKS</span></span>

[<span data-ttu-id="b6f9d-133">Get-AzureRmPowerBIWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="b6f9d-133">Get-AzureRmPowerBIWorkspaceCollection</span></span>](./Get-AzureRmPowerBIWorkspaceCollection.md)

[<span data-ttu-id="b6f9d-134">Remove-AzureRmPowerBIWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="b6f9d-134">Remove-AzureRmPowerBIWorkspaceCollection</span></span>](./Remove-AzureRmPowerBIWorkspaceCollection.md)


