---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/remove-aznetappfilesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesAccount.md
ms.openlocfilehash: 5f6e2421a20cb7aaf044d3abfbbddf7f5c72b37e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100147242"
---
# <span data-ttu-id="810ee-101">Remove-AzNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="810ee-101">Remove-AzNetAppFilesAccount</span></span>

## <span data-ttu-id="810ee-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="810ee-102">SYNOPSIS</span></span>
<span data-ttu-id="810ee-103">Töröl egy Azure NetApp-fájlt (ANF-fiókot).</span><span class="sxs-lookup"><span data-stu-id="810ee-103">Deletes an Azure NetApp Files (ANF) account.</span></span>

## <span data-ttu-id="810ee-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="810ee-104">SYNTAX</span></span>

### <span data-ttu-id="810ee-105">ByFieldsParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="810ee-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzNetAppFilesAccount -ResourceGroupName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="810ee-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="810ee-106">ByResourceIdParameterSet</span></span>
```
Remove-AzNetAppFilesAccount -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="810ee-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="810ee-107">ByObjectParameterSet</span></span>
```
Remove-AzNetAppFilesAccount -InputObject <PSNetAppFilesAccount> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="810ee-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="810ee-108">DESCRIPTION</span></span>
<span data-ttu-id="810ee-109">A **Remove-AzNetAppFilesAccount** parancsmag töröl egy ANF-fiókot.</span><span class="sxs-lookup"><span data-stu-id="810ee-109">The **Remove-AzNetAppFilesAccount** cmdlet deletes an ANF account.</span></span>

## <span data-ttu-id="810ee-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="810ee-110">EXAMPLES</span></span>

### <span data-ttu-id="810ee-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="810ee-111">Example 1</span></span>
```
PS C:\>Remove-AzNetAppFilesAccount -ResourceGroupName "MyRG" -Name "MyAnfAccount"
```

<span data-ttu-id="810ee-112">Ez a parancs törli a "MyAnfAccount" ANF-fiókot.</span><span class="sxs-lookup"><span data-stu-id="810ee-112">This command deletes the ANF account "MyAnfAccount".</span></span>

## <span data-ttu-id="810ee-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="810ee-113">PARAMETERS</span></span>

### <span data-ttu-id="810ee-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="810ee-114">-DefaultProfile</span></span>
<span data-ttu-id="810ee-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="810ee-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="810ee-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="810ee-116">-InputObject</span></span>
<span data-ttu-id="810ee-117">Az eltávolítható fiókobjektum</span><span class="sxs-lookup"><span data-stu-id="810ee-117">The account object to remove</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="810ee-118">-Name</span><span class="sxs-lookup"><span data-stu-id="810ee-118">-Name</span></span>
<span data-ttu-id="810ee-119">Az ANF-fiók neve</span><span class="sxs-lookup"><span data-stu-id="810ee-119">The name of the ANF account</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases: AccountName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="810ee-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="810ee-120">-PassThru</span></span>
<span data-ttu-id="810ee-121">Annak visszaadése, hogy a megadott fiók eltávolítása sikeresen megtörtént-e</span><span class="sxs-lookup"><span data-stu-id="810ee-121">Return whether the specified account was successfully removed</span></span>

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

### <span data-ttu-id="810ee-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="810ee-122">-ResourceGroupName</span></span>
<span data-ttu-id="810ee-123">Az ANF-fiók erőforráscsoportja</span><span class="sxs-lookup"><span data-stu-id="810ee-123">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="810ee-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="810ee-124">-ResourceId</span></span>
<span data-ttu-id="810ee-125">Az ANF-fiók erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="810ee-125">The resource id of the ANF account</span></span>

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

### <span data-ttu-id="810ee-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="810ee-126">-Confirm</span></span>
<span data-ttu-id="810ee-127">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="810ee-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="810ee-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="810ee-128">-WhatIf</span></span>
<span data-ttu-id="810ee-129">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="810ee-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="810ee-130">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="810ee-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="810ee-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="810ee-131">CommonParameters</span></span>
<span data-ttu-id="810ee-132">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="810ee-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="810ee-133">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="810ee-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="810ee-134">INPUTS</span><span class="sxs-lookup"><span data-stu-id="810ee-134">INPUTS</span></span>

### <span data-ttu-id="810ee-135">System.String</span><span class="sxs-lookup"><span data-stu-id="810ee-135">System.String</span></span>

### <span data-ttu-id="810ee-136">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="810ee-136">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

## <span data-ttu-id="810ee-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="810ee-137">OUTPUTS</span></span>

### <span data-ttu-id="810ee-138">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="810ee-138">System.Boolean</span></span>

## <span data-ttu-id="810ee-139">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="810ee-139">NOTES</span></span>

## <span data-ttu-id="810ee-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="810ee-140">RELATED LINKS</span></span>
