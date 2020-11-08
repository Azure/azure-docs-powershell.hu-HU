---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/remove-azdatashareaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShareAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShareAccount.md
ms.openlocfilehash: 0e8c3fac1c286845686d158c01217b0d4199639c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94017825"
---
# <span data-ttu-id="349b7-101">Remove-AzDataShareAccount</span><span class="sxs-lookup"><span data-stu-id="349b7-101">Remove-AzDataShareAccount</span></span>

## <span data-ttu-id="349b7-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="349b7-102">SYNOPSIS</span></span>
<span data-ttu-id="349b7-103">DataShare-fiók eltávolítása</span><span class="sxs-lookup"><span data-stu-id="349b7-103">Removes a datashare account</span></span>

## <span data-ttu-id="349b7-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="349b7-104">SYNTAX</span></span>

### <span data-ttu-id="349b7-105">ByFieldsParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="349b7-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzDataShareAccount -ResourceGroupName <String> -Name <String> [-PassThru] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="349b7-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="349b7-106">ByResourceIdParameterSet</span></span>
```
Remove-AzDataShareAccount -ResourceId <String> [-PassThru] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="349b7-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="349b7-107">ByObjectParameterSet</span></span>
```
Remove-AzDataShareAccount -InputObject <PSDataShareAccount> [-PassThru] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="349b7-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="349b7-108">DESCRIPTION</span></span>
<span data-ttu-id="349b7-109">A **Remove-AzDataShareAccount** parancsmag eltávolítja a DataShare-fiókot.</span><span class="sxs-lookup"><span data-stu-id="349b7-109">The **Remove-AzDataShareAccount** cmdlet removes a datashare account.</span></span>

## <span data-ttu-id="349b7-110">Példák</span><span class="sxs-lookup"><span data-stu-id="349b7-110">EXAMPLES</span></span>

### <span data-ttu-id="349b7-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="349b7-111">Example 1</span></span>
```
PS C:\> Remove-AzDataShareAccount -Name "WikiADS" -ResourceGroupName "ADS"
Confirm
Are you sure you want to remove datashare account 'WikiADS' in resource group 'ADS'? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
True
```

<span data-ttu-id="349b7-112">Ez a parancs eltávolítja a WikiADS nevű DataShare-fiókot a ADS nevű erőforráscsoport nevében.</span><span class="sxs-lookup"><span data-stu-id="349b7-112">This command removes the datashare account named WikiADS from the resource group named ADS.</span></span>
<span data-ttu-id="349b7-113">A parancs a $True értékét számítja ki.</span><span class="sxs-lookup"><span data-stu-id="349b7-113">This command returns a value of $True.</span></span>

## <span data-ttu-id="349b7-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="349b7-114">PARAMETERS</span></span>

### <span data-ttu-id="349b7-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="349b7-115">-AsJob</span></span>
<span data-ttu-id="349b7-116">{{Fill AsJob Description}}</span><span class="sxs-lookup"><span data-stu-id="349b7-116">{{Fill AsJob Description}}</span></span>

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

### <span data-ttu-id="349b7-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="349b7-117">-DefaultProfile</span></span>
<span data-ttu-id="349b7-118">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="349b7-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="349b7-119">-Force</span><span class="sxs-lookup"><span data-stu-id="349b7-119">-Force</span></span>
<span data-ttu-id="349b7-120">{{Fill Force Description}}</span><span class="sxs-lookup"><span data-stu-id="349b7-120">{{Fill Force Description}}</span></span>

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

### <span data-ttu-id="349b7-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="349b7-121">-InputObject</span></span>
<span data-ttu-id="349b7-122">Az Azure Data Share-fiók objektuma.</span><span class="sxs-lookup"><span data-stu-id="349b7-122">The azure data share account object.</span></span>


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

### <span data-ttu-id="349b7-123">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="349b7-123">-Name</span></span>
<span data-ttu-id="349b7-124">Azure Data Share-fiók neve</span><span class="sxs-lookup"><span data-stu-id="349b7-124">Azure data share account name.</span></span>

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

### <span data-ttu-id="349b7-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="349b7-125">-PassThru</span></span>
<span data-ttu-id="349b7-126">Visszatérési objektum (ha meg van adva)</span><span class="sxs-lookup"><span data-stu-id="349b7-126">Return object (if specified).</span></span>

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

### <span data-ttu-id="349b7-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="349b7-127">-ResourceGroupName</span></span>
<span data-ttu-id="349b7-128">Az Azure Data Share-fiók erőforráscsoport-neve.</span><span class="sxs-lookup"><span data-stu-id="349b7-128">The resource group name of azure data share account.</span></span>

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

### <span data-ttu-id="349b7-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="349b7-129">-ResourceId</span></span>
<span data-ttu-id="349b7-130">Az Azure Data Share-fiók erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="349b7-130">The resource id of the azure data share account.</span></span>

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

### <span data-ttu-id="349b7-131">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="349b7-131">-Confirm</span></span>
<span data-ttu-id="349b7-132">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="349b7-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="349b7-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="349b7-133">-WhatIf</span></span>
<span data-ttu-id="349b7-134">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="349b7-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="349b7-135">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="349b7-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="349b7-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="349b7-136">CommonParameters</span></span>
<span data-ttu-id="349b7-137">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="349b7-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="349b7-138">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="349b7-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="349b7-139">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="349b7-139">INPUTS</span></span>

### <span data-ttu-id="349b7-140">System. String</span><span class="sxs-lookup"><span data-stu-id="349b7-140">System.String</span></span>

### <span data-ttu-id="349b7-141">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareAccount</span><span class="sxs-lookup"><span data-stu-id="349b7-141">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareAccount</span></span>

## <span data-ttu-id="349b7-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="349b7-142">OUTPUTS</span></span>

### <span data-ttu-id="349b7-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="349b7-143">System.Boolean</span></span>

## <span data-ttu-id="349b7-144">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="349b7-144">NOTES</span></span>

## <span data-ttu-id="349b7-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="349b7-145">RELATED LINKS</span></span>
