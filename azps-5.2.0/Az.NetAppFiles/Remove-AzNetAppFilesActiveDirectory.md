---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/remove-aznetappfilesactivedirectory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesActiveDirectory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesActiveDirectory.md
ms.openlocfilehash: 7fcf1f749816872fb7407fedaea10d06f3385441
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98359867"
---
# <span data-ttu-id="55520-101">Remove-AzNetAppFilesActiveDirectory</span><span class="sxs-lookup"><span data-stu-id="55520-101">Remove-AzNetAppFilesActiveDirectory</span></span>

## <span data-ttu-id="55520-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="55520-102">SYNOPSIS</span></span>
<span data-ttu-id="55520-103">Törli az Azure NetApp-fájlok (ANF) active directory-konfigurációját.</span><span class="sxs-lookup"><span data-stu-id="55520-103">Deletes an Azure NetApp Files (ANF) active directory configuration.</span></span>

## <span data-ttu-id="55520-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="55520-104">SYNTAX</span></span>

### <span data-ttu-id="55520-105">ByFieldsParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="55520-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzNetAppFilesActiveDirectory -ResourceGroupName <String> -AccountName <String>
 -ActiveDirectoryId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="55520-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="55520-106">ByParentObjectParameterSet</span></span>
```
Remove-AzNetAppFilesActiveDirectory -ActiveDirectoryId <String> -AccountObject <PSNetAppFilesAccount>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="55520-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="55520-107">ByObjectParameterSet</span></span>
```
Remove-AzNetAppFilesActiveDirectory -InputObject <PSNetAppFilesActiveDirectory> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="55520-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="55520-108">DESCRIPTION</span></span>
<span data-ttu-id="55520-109">A **Remove-AzNetAppFilesActiveDirectory** parancsmag törli az ANF active directory-konfigurációt.</span><span class="sxs-lookup"><span data-stu-id="55520-109">The **Remove-AzNetAppFilesActiveDirectory** cmdlet deletes an ANF active directory configuration.</span></span>

## <span data-ttu-id="55520-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="55520-110">EXAMPLES</span></span>

### <span data-ttu-id="55520-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="55520-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzNetAppFilesActiveDirectory -ResourceGroupName "MyRG" -AccountName "MyAccount" -Name "MyADName"
```

<span data-ttu-id="55520-112">Ez a parancs törli az új ANF active directory-konfigurációt "MyADName" néven.</span><span class="sxs-lookup"><span data-stu-id="55520-112">This command deletes the new ANF active directory configuration with a the name "MyADName".</span></span>

## <span data-ttu-id="55520-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="55520-113">PARAMETERS</span></span>

### <span data-ttu-id="55520-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="55520-114">-AccountName</span></span>
<span data-ttu-id="55520-115">Az ANF-fiók neve</span><span class="sxs-lookup"><span data-stu-id="55520-115">The name of the ANF account</span></span>

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

### <span data-ttu-id="55520-116">-AccountObject</span><span class="sxs-lookup"><span data-stu-id="55520-116">-AccountObject</span></span>
<span data-ttu-id="55520-117">Az Active Directory-objektum fiókja</span><span class="sxs-lookup"><span data-stu-id="55520-117">The Account for the Active Directory object</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="55520-118">-ActiveDirectoryId</span><span class="sxs-lookup"><span data-stu-id="55520-118">-ActiveDirectoryId</span></span>
<span data-ttu-id="55520-119">Az ANF active directory azonosítója</span><span class="sxs-lookup"><span data-stu-id="55520-119">The ID of the ANF active directory</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet, ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="55520-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="55520-120">-DefaultProfile</span></span>
<span data-ttu-id="55520-121">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="55520-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="55520-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="55520-122">-InputObject</span></span>
<span data-ttu-id="55520-123">Az eltávolítható Active Directory-objektum</span><span class="sxs-lookup"><span data-stu-id="55520-123">The active directory object to remove</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesActiveDirectory
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="55520-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="55520-124">-PassThru</span></span>
<span data-ttu-id="55520-125">Visszaadja, hogy a megadott Active Directory-címtár eltávolítása sikeresen megtörtént-e</span><span class="sxs-lookup"><span data-stu-id="55520-125">Return whether the specified Active Directory  was successfully removed</span></span>

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

### <span data-ttu-id="55520-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="55520-126">-ResourceGroupName</span></span>
<span data-ttu-id="55520-127">Az ANF-fiók erőforráscsoportja</span><span class="sxs-lookup"><span data-stu-id="55520-127">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="55520-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="55520-128">-Confirm</span></span>
<span data-ttu-id="55520-129">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="55520-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="55520-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="55520-130">-WhatIf</span></span>
<span data-ttu-id="55520-131">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="55520-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="55520-132">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="55520-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="55520-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="55520-133">CommonParameters</span></span>
<span data-ttu-id="55520-134">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="55520-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="55520-135">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="55520-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="55520-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="55520-136">INPUTS</span></span>

### <span data-ttu-id="55520-137">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="55520-137">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

### <span data-ttu-id="55520-138">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesActiveDirectory</span><span class="sxs-lookup"><span data-stu-id="55520-138">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesActiveDirectory</span></span>

## <span data-ttu-id="55520-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="55520-139">OUTPUTS</span></span>

### <span data-ttu-id="55520-140">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesActiveDirectory</span><span class="sxs-lookup"><span data-stu-id="55520-140">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesActiveDirectory</span></span>

## <span data-ttu-id="55520-141">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="55520-141">NOTES</span></span>

## <span data-ttu-id="55520-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="55520-142">RELATED LINKS</span></span>
