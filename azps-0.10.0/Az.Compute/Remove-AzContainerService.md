---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 8180092D-5B1D-43A0-B830-D009B30E2DDF
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azcontainerservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Remove-AzContainerService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Remove-AzContainerService.md
ms.openlocfilehash: 4a83b1c23b3c0cb9cdd86fde6f8aac4bb13f91ba
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93844433"
---
# <span data-ttu-id="c6e49-101">Remove-AzContainerService</span><span class="sxs-lookup"><span data-stu-id="c6e49-101">Remove-AzContainerService</span></span>

## <span data-ttu-id="c6e49-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c6e49-102">SYNOPSIS</span></span>
<span data-ttu-id="c6e49-103">Tároló szolgáltatás eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="c6e49-103">Removes a container service.</span></span>

## <span data-ttu-id="c6e49-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c6e49-104">SYNTAX</span></span>

```
Remove-AzContainerService [-ResourceGroupName] <String> [-Name] <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c6e49-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="c6e49-105">DESCRIPTION</span></span>
<span data-ttu-id="c6e49-106">A **Remove-AzContainerService** parancsmag eltávolítja a tároló szolgáltatást az Azure-fiókjából.</span><span class="sxs-lookup"><span data-stu-id="c6e49-106">The **Remove-AzContainerService** cmdlet removes a container service from your Azure account.</span></span>

## <span data-ttu-id="c6e49-107">Példák</span><span class="sxs-lookup"><span data-stu-id="c6e49-107">EXAMPLES</span></span>

### <span data-ttu-id="c6e49-108">1. példa: tároló szolgáltatás eltávolítása</span><span class="sxs-lookup"><span data-stu-id="c6e49-108">Example 1: Remove a container service</span></span>
```
PS C:\> Remove-AzContainerService -ResourceGroupName "ResourceGroup17" -Name "CSResourceGroup17"
```

<span data-ttu-id="c6e49-109">Ez a parancs eltávolítja a CSResourceGroup17 nevű tároló szolgáltatást.</span><span class="sxs-lookup"><span data-stu-id="c6e49-109">This command removes the container service named CSResourceGroup17.</span></span>

## <span data-ttu-id="c6e49-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c6e49-110">PARAMETERS</span></span>

### <span data-ttu-id="c6e49-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c6e49-111">-AsJob</span></span>
<span data-ttu-id="c6e49-112">Futtassa a parancsmagot a háttérben, és a tevékenység visszaadása a folyamat nyomon követéséhez.</span><span class="sxs-lookup"><span data-stu-id="c6e49-112">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="c6e49-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c6e49-113">-DefaultProfile</span></span>
<span data-ttu-id="c6e49-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c6e49-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c6e49-115">-Force</span><span class="sxs-lookup"><span data-stu-id="c6e49-115">-Force</span></span>
<span data-ttu-id="c6e49-116">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="c6e49-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="c6e49-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="c6e49-117">-Name</span></span>
<span data-ttu-id="c6e49-118">Annak a tároló szolgáltatásnak a nevét adja meg, amelyre a parancsmag eltávolítja.</span><span class="sxs-lookup"><span data-stu-id="c6e49-118">Specifies the name of the container service that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c6e49-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c6e49-119">-ResourceGroupName</span></span>
<span data-ttu-id="c6e49-120">Annak a tároló szolgáltatásnak az erőforrás csoportját adja meg, amely a parancsmag eltávolítását okozta.</span><span class="sxs-lookup"><span data-stu-id="c6e49-120">Specifies the resource group of the container service that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c6e49-121">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="c6e49-121">-Confirm</span></span>
<span data-ttu-id="c6e49-122">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="c6e49-122">Prompts you for confirmation before running the cmdlet.</span></span>
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

### <span data-ttu-id="c6e49-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c6e49-123">-WhatIf</span></span>
<span data-ttu-id="c6e49-124">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="c6e49-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c6e49-125">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="c6e49-125">The cmdlet is not run.</span></span>
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

### <span data-ttu-id="c6e49-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c6e49-126">CommonParameters</span></span>
<span data-ttu-id="c6e49-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c6e49-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c6e49-128">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c6e49-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c6e49-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c6e49-129">INPUTS</span></span>

### <span data-ttu-id="c6e49-130">Nincs</span><span class="sxs-lookup"><span data-stu-id="c6e49-130">None</span></span>
<span data-ttu-id="c6e49-131">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="c6e49-131">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="c6e49-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c6e49-132">OUTPUTS</span></span>

### <span data-ttu-id="c6e49-133">System. Void</span><span class="sxs-lookup"><span data-stu-id="c6e49-133">System.Void</span></span>

## <span data-ttu-id="c6e49-134">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c6e49-134">NOTES</span></span>

## <span data-ttu-id="c6e49-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c6e49-135">RELATED LINKS</span></span>

[<span data-ttu-id="c6e49-136">Get-AzContainerService</span><span class="sxs-lookup"><span data-stu-id="c6e49-136">Get-AzContainerService</span></span>](./Get-AzContainerService.md)

[<span data-ttu-id="c6e49-137">Új – AzContainerService</span><span class="sxs-lookup"><span data-stu-id="c6e49-137">New-AzContainerService</span></span>](./New-AzContainerService.md)

[<span data-ttu-id="c6e49-138">Update-AzContainerService</span><span class="sxs-lookup"><span data-stu-id="c6e49-138">Update-AzContainerService</span></span>](./Update-AzContainerService.md)


