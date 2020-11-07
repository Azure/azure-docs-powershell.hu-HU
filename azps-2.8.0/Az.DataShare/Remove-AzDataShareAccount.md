---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/remove-azdatashareaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShareAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShareAccount.md
ms.openlocfilehash: 4888cacfbc92a38402bab089555ac6d6e7174038
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93666699"
---
# <span data-ttu-id="fd544-101">Remove-AzDataShareAccount</span><span class="sxs-lookup"><span data-stu-id="fd544-101">Remove-AzDataShareAccount</span></span>

## <span data-ttu-id="fd544-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="fd544-102">SYNOPSIS</span></span>
<span data-ttu-id="fd544-103">DataShare-fiók eltávolítása</span><span class="sxs-lookup"><span data-stu-id="fd544-103">Removes a datashare account</span></span>

## <span data-ttu-id="fd544-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="fd544-104">SYNTAX</span></span>

### <span data-ttu-id="fd544-105">ByFieldsParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="fd544-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzDataShareAccount -ResourceGroupName <String> -Name <String> [-PassThru] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fd544-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="fd544-106">ByResourceIdParameterSet</span></span>
```
Remove-AzDataShareAccount -ResourceId <String> [-PassThru] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fd544-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="fd544-107">ByObjectParameterSet</span></span>
```
Remove-AzDataShareAccount -InputObject <PSDataShareAccount> [-PassThru] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fd544-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="fd544-108">DESCRIPTION</span></span>
<span data-ttu-id="fd544-109">A **Remove-AzDataShareAccount** parancsmag eltávolítja a DataShare-fiókot.</span><span class="sxs-lookup"><span data-stu-id="fd544-109">The **Remove-AzDataShareAccount** cmdlet removes a datashare account.</span></span>

## <span data-ttu-id="fd544-110">Példák</span><span class="sxs-lookup"><span data-stu-id="fd544-110">EXAMPLES</span></span>

### <span data-ttu-id="fd544-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="fd544-111">Example 1</span></span>
```
PS C:\> Remove-AzDataShareAccount -Name "WikiADS" -ResourceGroupName "ADS"
Confirm
Are you sure you want to remove datashare account 'WikiADS' in resource group 'ADS'? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
True
```

<span data-ttu-id="fd544-112">Ez a parancs eltávolítja a WikiADS nevű DataShare-fiókot a ADS nevű erőforráscsoport nevében.</span><span class="sxs-lookup"><span data-stu-id="fd544-112">This command removes the datashare account named WikiADS from the resource group named ADS.</span></span>
<span data-ttu-id="fd544-113">A parancs a $True értékét számítja ki.</span><span class="sxs-lookup"><span data-stu-id="fd544-113">This command returns a value of $True.</span></span>

## <span data-ttu-id="fd544-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="fd544-114">PARAMETERS</span></span>

### <span data-ttu-id="fd544-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fd544-115">-AsJob</span></span>
<span data-ttu-id="fd544-116">{{Fill AsJob Description}}</span><span class="sxs-lookup"><span data-stu-id="fd544-116">{{Fill AsJob Description}}</span></span>

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

### <span data-ttu-id="fd544-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fd544-117">-DefaultProfile</span></span>
<span data-ttu-id="fd544-118">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="fd544-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fd544-119">-Force</span><span class="sxs-lookup"><span data-stu-id="fd544-119">-Force</span></span>
<span data-ttu-id="fd544-120">{{Fill Force Description}}</span><span class="sxs-lookup"><span data-stu-id="fd544-120">{{Fill Force Description}}</span></span>

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

### <span data-ttu-id="fd544-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fd544-121">-InputObject</span></span>
<span data-ttu-id="fd544-122">Az Azure Data Share-fiók objektuma.</span><span class="sxs-lookup"><span data-stu-id="fd544-122">The azure data share account object.</span></span>


```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareAccount
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fd544-123">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="fd544-123">-Name</span></span>
<span data-ttu-id="fd544-124">Azure Data Share-fiók neve</span><span class="sxs-lookup"><span data-stu-id="fd544-124">Azure data share account name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fd544-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fd544-125">-PassThru</span></span>
<span data-ttu-id="fd544-126">Visszatérési objektum (ha meg van adva)</span><span class="sxs-lookup"><span data-stu-id="fd544-126">Return object (if specified).</span></span>

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

### <span data-ttu-id="fd544-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fd544-127">-ResourceGroupName</span></span>
<span data-ttu-id="fd544-128">Az Azure Data Share-fiók erőforráscsoport-neve.</span><span class="sxs-lookup"><span data-stu-id="fd544-128">The resource group name of azure data share account.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fd544-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fd544-129">-ResourceId</span></span>
<span data-ttu-id="fd544-130">Az Azure Data Share-fiók erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="fd544-130">The resource id of the azure data share account.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fd544-131">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="fd544-131">-Confirm</span></span>
<span data-ttu-id="fd544-132">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="fd544-132">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fd544-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fd544-133">-WhatIf</span></span>
<span data-ttu-id="fd544-134">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="fd544-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fd544-135">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="fd544-135">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fd544-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fd544-136">CommonParameters</span></span>
<span data-ttu-id="fd544-137">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="fd544-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fd544-138">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fd544-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fd544-139">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="fd544-139">INPUTS</span></span>

### <span data-ttu-id="fd544-140">System. String</span><span class="sxs-lookup"><span data-stu-id="fd544-140">System.String</span></span>

### <span data-ttu-id="fd544-141">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareAccount</span><span class="sxs-lookup"><span data-stu-id="fd544-141">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareAccount</span></span>

## <span data-ttu-id="fd544-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="fd544-142">OUTPUTS</span></span>

### <span data-ttu-id="fd544-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="fd544-143">System.Boolean</span></span>

## <span data-ttu-id="fd544-144">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="fd544-144">NOTES</span></span>

## <span data-ttu-id="fd544-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="fd544-145">RELATED LINKS</span></span>
