---
external help file: Microsoft.Azure.Commands.Management.PowerBIEmbedded.dll-Help.xml
Module Name: AzureRM.PowerBIEmbedded
ms.assetid: 8FB2D9A0-BF7A-482D-B3A2-566FCA8C62A1
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.powerbiembedded/reset-azurermpowerbiworkspacecollectionaccesskeys
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.Management.PowerBIEmbedded/help/Reset-AzureRmPowerBIWorkspaceCollectionAccessKeys.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.Management.PowerBIEmbedded/help/Reset-AzureRmPowerBIWorkspaceCollectionAccessKeys.md
ms.openlocfilehash: 99a575d4eb17cc41eeea49f1db2a801bb6a28c98
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93492251"
---
# <span data-ttu-id="4683b-101">Reset-AzureRmPowerBIWorkspaceCollectionAccessKeys</span><span class="sxs-lookup"><span data-stu-id="4683b-101">Reset-AzureRmPowerBIWorkspaceCollectionAccessKeys</span></span>

## <span data-ttu-id="4683b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="4683b-102">SYNOPSIS</span></span>
<span data-ttu-id="4683b-103">A megadott Access-kulcs visszaállítása</span><span class="sxs-lookup"><span data-stu-id="4683b-103">Resets the specified access key.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4683b-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="4683b-104">SYNTAX</span></span>

```
Reset-AzureRmPowerBIWorkspaceCollectionAccessKeys [-ResourceGroupName] <String>
 [-WorkspaceCollectionName] <String> [-Key1] [-Key2] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4683b-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="4683b-105">DESCRIPTION</span></span>
<span data-ttu-id="4683b-106">A **reset-AzureRmPowerBIWorkspaceCollectionAccessKeys** parancsmag visszaállítja a megadott Access-kulcsot a Power bi-munkaterületi gyűjteményben.</span><span class="sxs-lookup"><span data-stu-id="4683b-106">The **Reset-AzureRmPowerBIWorkspaceCollectionAccessKeys** cmdlet resets the specified access key in your Power BI workspace collection.</span></span>

## <span data-ttu-id="4683b-107">Példák</span><span class="sxs-lookup"><span data-stu-id="4683b-107">EXAMPLES</span></span>

### <span data-ttu-id="4683b-108">1. példa: az elsődleges hozzáférés kulcsának alaphelyzetbe állítása</span><span class="sxs-lookup"><span data-stu-id="4683b-108">Example 1: Reset the primary access key</span></span>
```
PS C:\>Reset-AzureRmPowerBIWorkspaceCollectionAccessKeys -ResourceGroupName "ResourceGroup17" -WorkspaceCollectionName "WCN11" -Key1
```

<span data-ttu-id="4683b-109">Ez a parancs visszaállítja a megadott erőforráscsoport WCN11 nevű munkaterületi gyűjtemény elsődleges hozzáférési kulcsát.</span><span class="sxs-lookup"><span data-stu-id="4683b-109">This command resets the primary access key for the workspace collection named WCN11 in the specified resource group.</span></span>

## <span data-ttu-id="4683b-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="4683b-110">PARAMETERS</span></span>

### <span data-ttu-id="4683b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4683b-111">-DefaultProfile</span></span>
<span data-ttu-id="4683b-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="4683b-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4683b-113">-Key1</span><span class="sxs-lookup"><span data-stu-id="4683b-113">-Key1</span></span>
<span data-ttu-id="4683b-114">Azt jelzi, hogy ez a parancsmag visszaállítja az elsődleges hozzáférési kulcsot.</span><span class="sxs-lookup"><span data-stu-id="4683b-114">Indicates that this cmdlet resets the primary access key.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4683b-115">-Azonosító2</span><span class="sxs-lookup"><span data-stu-id="4683b-115">-Key2</span></span>
<span data-ttu-id="4683b-116">Azt jelzi, hogy ez a parancsmag visszaállítja a másodlagos elérési kulcsot.</span><span class="sxs-lookup"><span data-stu-id="4683b-116">Indicates that this cmdlet resets the secondary access key.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4683b-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4683b-117">-ResourceGroupName</span></span>
<span data-ttu-id="4683b-118">A gyűjtemény erőforráscsoport-csoportjának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="4683b-118">Specifies the name of the resource group of the collection.</span></span>

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

### <span data-ttu-id="4683b-119">-WorkspaceCollectionName</span><span class="sxs-lookup"><span data-stu-id="4683b-119">-WorkspaceCollectionName</span></span>
<span data-ttu-id="4683b-120">Annak a Power BI-munkaterületi gyűjteménynek a nevét adja meg, amelyen a parancsmag működik.</span><span class="sxs-lookup"><span data-stu-id="4683b-120">Specifies the name of the Power BI workspace collection on which this cmdlet operates.</span></span>

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

### <span data-ttu-id="4683b-121">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="4683b-121">-Confirm</span></span>
<span data-ttu-id="4683b-122">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="4683b-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4683b-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4683b-123">-WhatIf</span></span>
<span data-ttu-id="4683b-124">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="4683b-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4683b-125">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="4683b-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4683b-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4683b-126">CommonParameters</span></span>
<span data-ttu-id="4683b-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="4683b-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4683b-128">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4683b-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4683b-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="4683b-129">INPUTS</span></span>

### <span data-ttu-id="4683b-130">Nincs</span><span class="sxs-lookup"><span data-stu-id="4683b-130">None</span></span>
<span data-ttu-id="4683b-131">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="4683b-131">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="4683b-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4683b-132">OUTPUTS</span></span>

### <span data-ttu-id="4683b-133">Microsoft. Azure. Command. Management. PowerBIEmbedded. models. PSWorkspaceCollectionAccessKey</span><span class="sxs-lookup"><span data-stu-id="4683b-133">Microsoft.Azure.Commands.Management.PowerBIEmbedded.Models.PSWorkspaceCollectionAccessKey</span></span>

## <span data-ttu-id="4683b-134">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="4683b-134">NOTES</span></span>

## <span data-ttu-id="4683b-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4683b-135">RELATED LINKS</span></span>

[<span data-ttu-id="4683b-136">Get-AzureRmPowerBIWorkspaceCollectionAccessKeys</span><span class="sxs-lookup"><span data-stu-id="4683b-136">Get-AzureRmPowerBIWorkspaceCollectionAccessKeys</span></span>](./Get-AzureRmPowerBIWorkspaceCollectionAccessKeys.md)


