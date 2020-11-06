---
external help file: Microsoft.Azure.Commands.Management.PowerBIEmbedded.dll-Help.xml
Module Name: AzureRM.PowerBIEmbedded
ms.assetid: 8FB2D9A0-BF7A-482D-B3A2-566FCA8C62A1
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.Management.PowerBIEmbedded/help/Reset-AzureRmPowerBIWorkspaceCollectionAccessKeys.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.Management.PowerBIEmbedded/help/Reset-AzureRmPowerBIWorkspaceCollectionAccessKeys.md
ms.openlocfilehash: 766682df23beaa7c513ff54554a3ebd59a6d1537
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93504019"
---
# <span data-ttu-id="18019-101">Reset-AzureRmPowerBIWorkspaceCollectionAccessKeys</span><span class="sxs-lookup"><span data-stu-id="18019-101">Reset-AzureRmPowerBIWorkspaceCollectionAccessKeys</span></span>

## <span data-ttu-id="18019-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="18019-102">SYNOPSIS</span></span>
<span data-ttu-id="18019-103">A megadott Access-kulcs visszaállítása</span><span class="sxs-lookup"><span data-stu-id="18019-103">Resets the specified access key.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="18019-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="18019-104">SYNTAX</span></span>

```
Reset-AzureRmPowerBIWorkspaceCollectionAccessKeys [-ResourceGroupName] <String>
 [-WorkspaceCollectionName] <String> [-Key1] [-Key2] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="18019-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="18019-105">DESCRIPTION</span></span>
<span data-ttu-id="18019-106">A **reset-AzureRmPowerBIWorkspaceCollectionAccessKeys** parancsmag visszaállítja a megadott Access-kulcsot a Power bi-munkaterületi gyűjteményben.</span><span class="sxs-lookup"><span data-stu-id="18019-106">The **Reset-AzureRmPowerBIWorkspaceCollectionAccessKeys** cmdlet resets the specified access key in your Power BI workspace collection.</span></span>

## <span data-ttu-id="18019-107">Példák</span><span class="sxs-lookup"><span data-stu-id="18019-107">EXAMPLES</span></span>

### <span data-ttu-id="18019-108">1. példa: az elsődleges hozzáférés kulcsának alaphelyzetbe állítása</span><span class="sxs-lookup"><span data-stu-id="18019-108">Example 1: Reset the primary access key</span></span>
```
PS C:\>Reset-AzureRmPowerBIWorkspaceCollectionAccessKeys -ResourceGroupName "ResourceGroup17" -WorkspaceCollectionName "WCN11" -Key1
```

<span data-ttu-id="18019-109">Ez a parancs visszaállítja a megadott erőforráscsoport WCN11 nevű munkaterületi gyűjtemény elsődleges hozzáférési kulcsát.</span><span class="sxs-lookup"><span data-stu-id="18019-109">This command resets the primary access key for the workspace collection named WCN11 in the specified resource group.</span></span>

## <span data-ttu-id="18019-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="18019-110">PARAMETERS</span></span>

### <span data-ttu-id="18019-111">-Key1</span><span class="sxs-lookup"><span data-stu-id="18019-111">-Key1</span></span>
<span data-ttu-id="18019-112">Azt jelzi, hogy ez a parancsmag visszaállítja az elsődleges hozzáférési kulcsot.</span><span class="sxs-lookup"><span data-stu-id="18019-112">Indicates that this cmdlet resets the primary access key.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18019-113">-Azonosító2</span><span class="sxs-lookup"><span data-stu-id="18019-113">-Key2</span></span>
<span data-ttu-id="18019-114">Azt jelzi, hogy ez a parancsmag visszaállítja a másodlagos elérési kulcsot.</span><span class="sxs-lookup"><span data-stu-id="18019-114">Indicates that this cmdlet resets the secondary access key.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18019-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="18019-115">-ResourceGroupName</span></span>
<span data-ttu-id="18019-116">A gyűjtemény erőforráscsoport-csoportjának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="18019-116">Specifies the name of the resource group of the collection.</span></span>

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

### <span data-ttu-id="18019-117">-WorkspaceCollectionName</span><span class="sxs-lookup"><span data-stu-id="18019-117">-WorkspaceCollectionName</span></span>
<span data-ttu-id="18019-118">Annak a Power BI-munkaterületi gyűjteménynek a nevét adja meg, amelyen a parancsmag működik.</span><span class="sxs-lookup"><span data-stu-id="18019-118">Specifies the name of the Power BI workspace collection on which this cmdlet operates.</span></span>

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

### <span data-ttu-id="18019-119">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="18019-119">-Confirm</span></span>
<span data-ttu-id="18019-120">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="18019-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="18019-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="18019-121">-WhatIf</span></span>
<span data-ttu-id="18019-122">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="18019-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="18019-123">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="18019-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="18019-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="18019-124">-DefaultProfile</span></span>
<span data-ttu-id="18019-125">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="18019-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="18019-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="18019-126">CommonParameters</span></span>
<span data-ttu-id="18019-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="18019-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="18019-128">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="18019-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="18019-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="18019-129">INPUTS</span></span>

## <span data-ttu-id="18019-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="18019-130">OUTPUTS</span></span>

### <span data-ttu-id="18019-131">Microsoft. Azure. Command. Management. PowerBIEmbedded. models. PSWorkspaceCollectionAccessKey</span><span class="sxs-lookup"><span data-stu-id="18019-131">Microsoft.Azure.Commands.Management.PowerBIEmbedded.Models.PSWorkspaceCollectionAccessKey</span></span>

## <span data-ttu-id="18019-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="18019-132">NOTES</span></span>

## <span data-ttu-id="18019-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="18019-133">RELATED LINKS</span></span>

[<span data-ttu-id="18019-134">Get-AzureRmPowerBIWorkspaceCollectionAccessKeys</span><span class="sxs-lookup"><span data-stu-id="18019-134">Get-AzureRmPowerBIWorkspaceCollectionAccessKeys</span></span>](./Get-AzureRmPowerBIWorkspaceCollectionAccessKeys.md)


