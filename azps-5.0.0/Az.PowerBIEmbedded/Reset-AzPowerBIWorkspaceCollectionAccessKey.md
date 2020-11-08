---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PowerBIEmbedded.dll-Help.xml
Module Name: Az.PowerBIEmbedded
ms.assetid: 8FB2D9A0-BF7A-482D-B3A2-566FCA8C62A1
online version: https://docs.microsoft.com/en-us/powershell/module/az.powerbiembedded/reset-azpowerbiworkspacecollectionaccesskey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Reset-AzPowerBIWorkspaceCollectionAccessKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Reset-AzPowerBIWorkspaceCollectionAccessKey.md
ms.openlocfilehash: d9e30c81eb0e2422b91be79bcfc7c732291c30cb
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94188063"
---
# <span data-ttu-id="4e8ec-101">Reset-AzPowerBIWorkspaceCollectionAccessKey</span><span class="sxs-lookup"><span data-stu-id="4e8ec-101">Reset-AzPowerBIWorkspaceCollectionAccessKey</span></span>

## <span data-ttu-id="4e8ec-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="4e8ec-102">SYNOPSIS</span></span>
<span data-ttu-id="4e8ec-103">A megadott Access-kulcs visszaállítása</span><span class="sxs-lookup"><span data-stu-id="4e8ec-103">Resets the specified access key.</span></span>

## <span data-ttu-id="4e8ec-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="4e8ec-104">SYNTAX</span></span>

```
Reset-AzPowerBIWorkspaceCollectionAccessKey [-ResourceGroupName] <String> [-WorkspaceCollectionName] <String>
 [-Key1] [-Key2] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4e8ec-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="4e8ec-105">DESCRIPTION</span></span>
<span data-ttu-id="4e8ec-106">A **reset-AzPowerBIWorkspaceCollectionAccessKey** parancsmag visszaállítja a megadott Access-kulcsot a Power bi-munkaterületi gyűjteményben.</span><span class="sxs-lookup"><span data-stu-id="4e8ec-106">The **Reset-AzPowerBIWorkspaceCollectionAccessKey** cmdlet resets the specified access key in your Power BI workspace collection.</span></span>

## <span data-ttu-id="4e8ec-107">Példák</span><span class="sxs-lookup"><span data-stu-id="4e8ec-107">EXAMPLES</span></span>

### <span data-ttu-id="4e8ec-108">1. példa: az elsődleges hozzáférés kulcsának alaphelyzetbe állítása</span><span class="sxs-lookup"><span data-stu-id="4e8ec-108">Example 1: Reset the primary access key</span></span>
```
PS C:\>Reset-AzPowerBIWorkspaceCollectionAccessKey -ResourceGroupName "ResourceGroup17" -WorkspaceCollectionName "WCN11" -Key1
```

<span data-ttu-id="4e8ec-109">Ez a parancs visszaállítja a megadott erőforráscsoport WCN11 nevű munkaterületi gyűjtemény elsődleges hozzáférési kulcsát.</span><span class="sxs-lookup"><span data-stu-id="4e8ec-109">This command resets the primary access key for the workspace collection named WCN11 in the specified resource group.</span></span>

## <span data-ttu-id="4e8ec-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="4e8ec-110">PARAMETERS</span></span>

### <span data-ttu-id="4e8ec-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4e8ec-111">-DefaultProfile</span></span>
<span data-ttu-id="4e8ec-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="4e8ec-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4e8ec-113">-Key1</span><span class="sxs-lookup"><span data-stu-id="4e8ec-113">-Key1</span></span>
<span data-ttu-id="4e8ec-114">Azt jelzi, hogy ez a parancsmag visszaállítja az elsődleges hozzáférési kulcsot.</span><span class="sxs-lookup"><span data-stu-id="4e8ec-114">Indicates that this cmdlet resets the primary access key.</span></span>

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

### <span data-ttu-id="4e8ec-115">-Azonosító2</span><span class="sxs-lookup"><span data-stu-id="4e8ec-115">-Key2</span></span>
<span data-ttu-id="4e8ec-116">Azt jelzi, hogy ez a parancsmag visszaállítja a másodlagos elérési kulcsot.</span><span class="sxs-lookup"><span data-stu-id="4e8ec-116">Indicates that this cmdlet resets the secondary access key.</span></span>

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

### <span data-ttu-id="4e8ec-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4e8ec-117">-ResourceGroupName</span></span>
<span data-ttu-id="4e8ec-118">A gyűjtemény erőforráscsoport-csoportjának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="4e8ec-118">Specifies the name of the resource group of the collection.</span></span>

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

### <span data-ttu-id="4e8ec-119">-WorkspaceCollectionName</span><span class="sxs-lookup"><span data-stu-id="4e8ec-119">-WorkspaceCollectionName</span></span>
<span data-ttu-id="4e8ec-120">Annak a Power BI-munkaterületi gyűjteménynek a nevét adja meg, amelyen a parancsmag működik.</span><span class="sxs-lookup"><span data-stu-id="4e8ec-120">Specifies the name of the Power BI workspace collection on which this cmdlet operates.</span></span>

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

### <span data-ttu-id="4e8ec-121">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="4e8ec-121">-Confirm</span></span>
<span data-ttu-id="4e8ec-122">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="4e8ec-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4e8ec-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4e8ec-123">-WhatIf</span></span>
<span data-ttu-id="4e8ec-124">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="4e8ec-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4e8ec-125">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="4e8ec-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4e8ec-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4e8ec-126">CommonParameters</span></span>
<span data-ttu-id="4e8ec-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="4e8ec-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4e8ec-128">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4e8ec-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4e8ec-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="4e8ec-129">INPUTS</span></span>

### <span data-ttu-id="4e8ec-130">System. String</span><span class="sxs-lookup"><span data-stu-id="4e8ec-130">System.String</span></span>

## <span data-ttu-id="4e8ec-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4e8ec-131">OUTPUTS</span></span>

### <span data-ttu-id="4e8ec-132">Microsoft. Azure. Command. Management. PowerBIEmbedded. models. PSWorkspaceCollectionAccessKey</span><span class="sxs-lookup"><span data-stu-id="4e8ec-132">Microsoft.Azure.Commands.Management.PowerBIEmbedded.Models.PSWorkspaceCollectionAccessKey</span></span>

## <span data-ttu-id="4e8ec-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="4e8ec-133">NOTES</span></span>

## <span data-ttu-id="4e8ec-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4e8ec-134">RELATED LINKS</span></span>

[<span data-ttu-id="4e8ec-135">Get-AzPowerBIWorkspaceCollectionAccessKey</span><span class="sxs-lookup"><span data-stu-id="4e8ec-135">Get-AzPowerBIWorkspaceCollectionAccessKey</span></span>](./Get-AzPowerBIWorkspaceCollectionAccessKey.md)


