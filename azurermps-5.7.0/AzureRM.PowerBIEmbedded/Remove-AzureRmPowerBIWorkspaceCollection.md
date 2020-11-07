---
external help file: Microsoft.Azure.Commands.Management.PowerBIEmbedded.dll-Help.xml
Module Name: AzureRM.PowerBIEmbedded
ms.assetid: 2D63CC6D-AB02-4299-A922-4057D6F595D7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.powerbiembedded/remove-azurermpowerbiworkspacecollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.Management.PowerBIEmbedded/help/Remove-AzureRmPowerBIWorkspaceCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.Management.PowerBIEmbedded/help/Remove-AzureRmPowerBIWorkspaceCollection.md
ms.openlocfilehash: 7f3a48db5d8f1e6c7b4b0e73b705fc375a0b514f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93679729"
---
# <span data-ttu-id="d7dbf-101">Remove-AzureRmPowerBIWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="d7dbf-101">Remove-AzureRmPowerBIWorkspaceCollection</span></span>

## <span data-ttu-id="d7dbf-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d7dbf-102">SYNOPSIS</span></span>
<span data-ttu-id="d7dbf-103">A Power BI-munkaterületi gyűjtemény eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="d7dbf-103">Removes a Power BI workspace collection.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d7dbf-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d7dbf-104">SYNTAX</span></span>

```
Remove-AzureRmPowerBIWorkspaceCollection [-ResourceGroupName] <String> [-WorkspaceCollectionName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d7dbf-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="d7dbf-105">DESCRIPTION</span></span>
<span data-ttu-id="d7dbf-106">A **Remove-AzureRmPowerBIWorkspaceCollection** parancsmag eltávolítja a Power bi-munkaterületi gyűjteményt az Azure-előfizetésből és az erőforrás-csoportból.</span><span class="sxs-lookup"><span data-stu-id="d7dbf-106">The **Remove-AzureRmPowerBIWorkspaceCollection** cmdlet removes a Power BI workspace collection from your Azure subscription and resource group.</span></span>

## <span data-ttu-id="d7dbf-107">Példák</span><span class="sxs-lookup"><span data-stu-id="d7dbf-107">EXAMPLES</span></span>

### <span data-ttu-id="d7dbf-108">1. példa: munkaterületi gyűjtemény eltávolítása</span><span class="sxs-lookup"><span data-stu-id="d7dbf-108">Example 1: Remove a workspace collection</span></span>
```
PS C:\>Remove-AzureRmPowerBIWorkspaceCollection -ResourceGroupName "ResourceGroup17" -WorkspaceCollectionName "WCN11"
```

<span data-ttu-id="d7dbf-109">Ez a parancs eltávolítja a megadott erőforráscsoport WCN11 nevű munkaterületi gyűjteményét.</span><span class="sxs-lookup"><span data-stu-id="d7dbf-109">This command removes the workspace collection named WCN11 in the specified resource group.</span></span>

## <span data-ttu-id="d7dbf-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d7dbf-110">PARAMETERS</span></span>

### <span data-ttu-id="d7dbf-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d7dbf-111">-DefaultProfile</span></span>
<span data-ttu-id="d7dbf-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="d7dbf-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d7dbf-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d7dbf-113">-ResourceGroupName</span></span>
<span data-ttu-id="d7dbf-114">Annak az erőforrás-csoportnak a neve, amelyből a parancsmag eltávolítja a munkaterületi gyűjteményt.</span><span class="sxs-lookup"><span data-stu-id="d7dbf-114">Specifies the name of the resource group from which this cmdlet removes a workspace collection.</span></span>

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

### <span data-ttu-id="d7dbf-115">-WorkspaceCollectionName</span><span class="sxs-lookup"><span data-stu-id="d7dbf-115">-WorkspaceCollectionName</span></span>
<span data-ttu-id="d7dbf-116">A parancsmag által eltávolított Power BI-munkaterületi gyűjtemény nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="d7dbf-116">Specifies the name of the Power BI workspace collection that this cmdlet removes.</span></span>

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

### <span data-ttu-id="d7dbf-117">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="d7dbf-117">-Confirm</span></span>
<span data-ttu-id="d7dbf-118">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="d7dbf-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7dbf-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d7dbf-119">-WhatIf</span></span>
<span data-ttu-id="d7dbf-120">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="d7dbf-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d7dbf-121">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="d7dbf-121">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7dbf-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d7dbf-122">CommonParameters</span></span>
<span data-ttu-id="d7dbf-123">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d7dbf-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d7dbf-124">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d7dbf-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d7dbf-125">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d7dbf-125">INPUTS</span></span>

### <span data-ttu-id="d7dbf-126">Nincs</span><span class="sxs-lookup"><span data-stu-id="d7dbf-126">None</span></span>
<span data-ttu-id="d7dbf-127">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="d7dbf-127">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="d7dbf-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d7dbf-128">OUTPUTS</span></span>

## <span data-ttu-id="d7dbf-129">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d7dbf-129">NOTES</span></span>

## <span data-ttu-id="d7dbf-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d7dbf-130">RELATED LINKS</span></span>

[<span data-ttu-id="d7dbf-131">Get-AzureRmPowerBIWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="d7dbf-131">Get-AzureRmPowerBIWorkspaceCollection</span></span>](./Get-AzureRmPowerBIWorkspaceCollection.md)

[<span data-ttu-id="d7dbf-132">Új – AzureRmPowerBIWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="d7dbf-132">New-AzureRmPowerBIWorkspaceCollection</span></span>](./New-AzureRmPowerBIWorkspaceCollection.md)


