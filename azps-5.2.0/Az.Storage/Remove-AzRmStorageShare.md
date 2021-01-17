---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/remove-azrmstorageshare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzRmStorageShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzRmStorageShare.md
ms.openlocfilehash: bff7a79513cc8eb0047860f9edd00c6c37c5f1b0
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98349397"
---
# <span data-ttu-id="9d5b6-101">Remove-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="9d5b6-101">Remove-AzRmStorageShare</span></span>

## <span data-ttu-id="9d5b6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9d5b6-102">SYNOPSIS</span></span>
<span data-ttu-id="9d5b6-103">Eltávolítja a tárhelyfájl megosztását.</span><span class="sxs-lookup"><span data-stu-id="9d5b6-103">Removes a Storage file share.</span></span>

## <span data-ttu-id="9d5b6-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="9d5b6-104">SYNTAX</span></span>

### <span data-ttu-id="9d5b6-105">AccountName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="9d5b6-105">AccountName (Default)</span></span>
```
Remove-AzRmStorageShare [-ResourceGroupName] <String> [-StorageAccountName] <String> -Name <String> [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9d5b6-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="9d5b6-106">AccountObject</span></span>
```
Remove-AzRmStorageShare -Name <String> -StorageAccount <PSStorageAccount> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9d5b6-107">ShareResourceId</span><span class="sxs-lookup"><span data-stu-id="9d5b6-107">ShareResourceId</span></span>
```
Remove-AzRmStorageShare [-ResourceId] <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9d5b6-108">ShareObject</span><span class="sxs-lookup"><span data-stu-id="9d5b6-108">ShareObject</span></span>
```
Remove-AzRmStorageShare -InputObject <PSShare> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9d5b6-109">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="9d5b6-109">DESCRIPTION</span></span>
<span data-ttu-id="9d5b6-110">A **New-AzRmStorageShare** parancsmag eltávolítja a tárhelyfájl megosztását.</span><span class="sxs-lookup"><span data-stu-id="9d5b6-110">The **New-AzRmStorageShare** cmdlet removes a Storage file share.</span></span>

## <span data-ttu-id="9d5b6-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="9d5b6-111">EXAMPLES</span></span>

### <span data-ttu-id="9d5b6-112">1. példa: Tárterületfájl-megosztás eltávolítása a Tárfiók nevével és a megosztás nevével</span><span class="sxs-lookup"><span data-stu-id="9d5b6-112">Example 1: Remove a Storage file share with Storage account name and share name</span></span>
```
PS C:\>Remove-AzRmStorageShare -ResourceGroupName "myResourceGroup" -StorageAccountName "myStorageAccount" -Name "myshare"
```

<span data-ttu-id="9d5b6-113">Ez a parancs eltávolítja a Tárterületfájl-megosztást a Tárfiók nevével és a megosztás nevével.</span><span class="sxs-lookup"><span data-stu-id="9d5b6-113">This command removes a Storage file share with Storage account name and share name.</span></span>

### <span data-ttu-id="9d5b6-114">2. példa: Tárterületfájl-megosztás eltávolítása a Tárfiók objektummal és a megosztás neve</span><span class="sxs-lookup"><span data-stu-id="9d5b6-114">Example 2: Remove a Storage file share with Storage account object and share name</span></span>
```
PS C:\>$accountObject = Get-AzStorageAccount -ResourceGroupName "myResourceGroup" -StorageAccountName "myStorageAccount"
PS C:\>Remove-AzRmStorageShare -StorageAccount $accountObject -Name "myshare"
```

<span data-ttu-id="9d5b6-115">Ez a parancs eltávolítja a Tárfiók-objektummal és a megosztás nevével együtt a tárfájl megosztását.</span><span class="sxs-lookup"><span data-stu-id="9d5b6-115">This command removes a Storage file share with Storage account object and share name.</span></span>

### <span data-ttu-id="9d5b6-116">3. példa: A tárfiók összes tárfájlmegosztásának eltávolítása folyamatban</span><span class="sxs-lookup"><span data-stu-id="9d5b6-116">Example 3: Remove all Storage file shares in a Storage account with pipeline</span></span>
```
PS C:\>Get-AzStorageShare -ResourceGroupName "myResourceGroup" -StorageAccountName "myStorageAccount" | Remove-AzRmStorageShare -Force
```

<span data-ttu-id="9d5b6-117">Ez a parancs eltávolítja a tárterületfájl-megosztásokat egy folyamatban futó Tárfiókban.</span><span class="sxs-lookup"><span data-stu-id="9d5b6-117">This command removes all Storage file shares in a Storage account with pipeline.</span></span>

## <span data-ttu-id="9d5b6-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9d5b6-118">PARAMETERS</span></span>

### <span data-ttu-id="9d5b6-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9d5b6-119">-DefaultProfile</span></span>
<span data-ttu-id="9d5b6-120">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="9d5b6-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9d5b6-121">-Force</span><span class="sxs-lookup"><span data-stu-id="9d5b6-121">-Force</span></span>
<span data-ttu-id="9d5b6-122">A Megosztás és az abban található összes tartalom eltávolítása kényszerítve</span><span class="sxs-lookup"><span data-stu-id="9d5b6-122">Force to remove the Share and all content in it</span></span>

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

### <span data-ttu-id="9d5b6-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9d5b6-123">-InputObject</span></span>
<span data-ttu-id="9d5b6-124">Tárterület megosztása objektum</span><span class="sxs-lookup"><span data-stu-id="9d5b6-124">Storage Share object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSShare
Parameter Sets: ShareObject
Aliases: Share

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9d5b6-125">-Name</span><span class="sxs-lookup"><span data-stu-id="9d5b6-125">-Name</span></span>
<span data-ttu-id="9d5b6-126">Név megosztása</span><span class="sxs-lookup"><span data-stu-id="9d5b6-126">Share Name</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName, AccountObject
Aliases: N, ShareName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d5b6-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9d5b6-127">-PassThru</span></span>
<span data-ttu-id="9d5b6-128">Azt jelzi, hogy ez a parancsmag egy **logikai** értéket ad vissza, amely tükrözi a művelet sikeres működését.</span><span class="sxs-lookup"><span data-stu-id="9d5b6-128">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="9d5b6-129">Alapértelmezés szerint ez a parancsmag nem ad vissza értéket.</span><span class="sxs-lookup"><span data-stu-id="9d5b6-129">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="9d5b6-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9d5b6-130">-ResourceGroupName</span></span>
<span data-ttu-id="9d5b6-131">Erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="9d5b6-131">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d5b6-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9d5b6-132">-ResourceId</span></span>
<span data-ttu-id="9d5b6-133">Fájlmegosztási erőforrás-azonosító bevitele</span><span class="sxs-lookup"><span data-stu-id="9d5b6-133">Input a File Share Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ShareResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9d5b6-134">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="9d5b6-134">-StorageAccount</span></span>
<span data-ttu-id="9d5b6-135">Tárfiók objektum</span><span class="sxs-lookup"><span data-stu-id="9d5b6-135">Storage account object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount
Parameter Sets: AccountObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9d5b6-136">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="9d5b6-136">-StorageAccountName</span></span>
<span data-ttu-id="9d5b6-137">Tárfiók neve.</span><span class="sxs-lookup"><span data-stu-id="9d5b6-137">Storage Account Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName
Aliases: AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d5b6-138">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9d5b6-138">-Confirm</span></span>
<span data-ttu-id="9d5b6-139">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="9d5b6-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9d5b6-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9d5b6-140">-WhatIf</span></span>
<span data-ttu-id="9d5b6-141">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="9d5b6-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9d5b6-142">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="9d5b6-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9d5b6-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9d5b6-143">CommonParameters</span></span>
<span data-ttu-id="9d5b6-144">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9d5b6-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9d5b6-145">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9d5b6-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9d5b6-146">INPUTS</span><span class="sxs-lookup"><span data-stu-id="9d5b6-146">INPUTS</span></span>

### <span data-ttu-id="9d5b6-147">System.String</span><span class="sxs-lookup"><span data-stu-id="9d5b6-147">System.String</span></span>

### <span data-ttu-id="9d5b6-148">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="9d5b6-148">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="9d5b6-149">Microsoft.Azure.Commands.Management.Storage.Models.PSShare</span><span class="sxs-lookup"><span data-stu-id="9d5b6-149">Microsoft.Azure.Commands.Management.Storage.Models.PSShare</span></span>

## <span data-ttu-id="9d5b6-150">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9d5b6-150">OUTPUTS</span></span>

### <span data-ttu-id="9d5b6-151">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="9d5b6-151">System.Boolean</span></span>

## <span data-ttu-id="9d5b6-152">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="9d5b6-152">NOTES</span></span>

## <span data-ttu-id="9d5b6-153">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9d5b6-153">RELATED LINKS</span></span>
