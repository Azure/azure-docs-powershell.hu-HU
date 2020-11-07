---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/remove-azrmstorageshare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzRmStorageShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzRmStorageShare.md
ms.openlocfilehash: 3c4071d11e521476f02cadb7323267f84183510b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93839784"
---
# <span data-ttu-id="388dc-101">Remove-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="388dc-101">Remove-AzRmStorageShare</span></span>

## <span data-ttu-id="388dc-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="388dc-102">SYNOPSIS</span></span>
<span data-ttu-id="388dc-103">Eltávolít egy tárterület-megosztást.</span><span class="sxs-lookup"><span data-stu-id="388dc-103">Removes a Storage file share.</span></span>

## <span data-ttu-id="388dc-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="388dc-104">SYNTAX</span></span>

### <span data-ttu-id="388dc-105">AccountName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="388dc-105">AccountName (Default)</span></span>
```
Remove-AzRmStorageShare [-ResourceGroupName] <String> [-StorageAccountName] <String> -Name <String> [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="388dc-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="388dc-106">AccountObject</span></span>
```
Remove-AzRmStorageShare -Name <String> -StorageAccount <PSStorageAccount> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="388dc-107">ShareResourceId</span><span class="sxs-lookup"><span data-stu-id="388dc-107">ShareResourceId</span></span>
```
Remove-AzRmStorageShare [-ResourceId] <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="388dc-108">ShareObject</span><span class="sxs-lookup"><span data-stu-id="388dc-108">ShareObject</span></span>
```
Remove-AzRmStorageShare -InputObject <PSShare> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="388dc-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="388dc-109">DESCRIPTION</span></span>
<span data-ttu-id="388dc-110">A **New-AzRmStorageShare** parancsmag eltávolítja a tárterület-megosztást.</span><span class="sxs-lookup"><span data-stu-id="388dc-110">The **New-AzRmStorageShare** cmdlet removes a Storage file share.</span></span>

## <span data-ttu-id="388dc-111">Példák</span><span class="sxs-lookup"><span data-stu-id="388dc-111">EXAMPLES</span></span>

### <span data-ttu-id="388dc-112">1. példa: tárterület-megosztás eltávolítása a tárolási fiók nevével és a megosztási névvel</span><span class="sxs-lookup"><span data-stu-id="388dc-112">Example 1: Remove a Storage file share with Storage account name and share name</span></span>
```
PS C:\>Remove-AzRmStorageShare -ResourceGroupName "myResourceGroup" -StorageAccountName "myStorageAccount" -Name "myshare"
```

<span data-ttu-id="388dc-113">Ez a parancs eltávolítja a tárterület-megosztást a tárolási fiók nevével és a megosztási névvel.</span><span class="sxs-lookup"><span data-stu-id="388dc-113">This command removes a Storage file share with Storage account name and share name.</span></span>

### <span data-ttu-id="388dc-114">2. példa: tárterület-megosztás eltávolítása a Storage Account objektummal és a megosztási névvel</span><span class="sxs-lookup"><span data-stu-id="388dc-114">Example 2: Remove a Storage file share with Storage account object and share name</span></span>
```
PS C:\>$accountObject = Get-AzStorageAccount -ResourceGroupName "myResourceGroup" -StorageAccountName "myStorageAccount"
PS C:\>Remove-AzRmStorageShare -StorageAccount $accountObject -Name "myshare"
```

<span data-ttu-id="388dc-115">Ez a parancs eltávolítja a tárterület-megosztást a Storage Account objektummal és a megosztási névvel.</span><span class="sxs-lookup"><span data-stu-id="388dc-115">This command removes a Storage file share with Storage account object and share name.</span></span>

### <span data-ttu-id="388dc-116">3. példa: az összes tárterület-megosztás eltávolítása a tároló fiókban</span><span class="sxs-lookup"><span data-stu-id="388dc-116">Example 3: Remove all Storage file shares in a Storage account with pipeline</span></span>
```
PS C:\>Get-AzStorageShare -ResourceGroupName "myResourceGroup" -StorageAccountName "myStorageAccount" | Remove-AzRmStorageShare -Force
```

<span data-ttu-id="388dc-117">Ez a parancs eltávolítja az összes tárterület-megosztást a tároló fiókban a csővezetéken.</span><span class="sxs-lookup"><span data-stu-id="388dc-117">This command removes all Storage file shares in a Storage account with pipeline.</span></span>

## <span data-ttu-id="388dc-118">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="388dc-118">PARAMETERS</span></span>

### <span data-ttu-id="388dc-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="388dc-119">-DefaultProfile</span></span>
<span data-ttu-id="388dc-120">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="388dc-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="388dc-121">-Force</span><span class="sxs-lookup"><span data-stu-id="388dc-121">-Force</span></span>
<span data-ttu-id="388dc-122">A megosztás és az összes tartalom eltávolításának kényszerítése</span><span class="sxs-lookup"><span data-stu-id="388dc-122">Force to remove the Share and all content in it</span></span>

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

### <span data-ttu-id="388dc-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="388dc-123">-InputObject</span></span>
<span data-ttu-id="388dc-124">Tárterület-megosztás objektum</span><span class="sxs-lookup"><span data-stu-id="388dc-124">Storage Share object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSShare
Parameter Sets: ShareObject
Aliases: Share

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="388dc-125">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="388dc-125">-Name</span></span>
<span data-ttu-id="388dc-126">Megosztás neve</span><span class="sxs-lookup"><span data-stu-id="388dc-126">Share Name</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName, AccountObject
Aliases: N, ShareName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="388dc-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="388dc-127">-PassThru</span></span>
<span data-ttu-id="388dc-128">Jelzi, hogy ez a parancsmag olyan **logikai** értéket ad eredményül, amely tükrözi a művelet sikerét.</span><span class="sxs-lookup"><span data-stu-id="388dc-128">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="388dc-129">Ez a parancsmag alapértelmezés szerint nem ad vissza értéket.</span><span class="sxs-lookup"><span data-stu-id="388dc-129">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="388dc-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="388dc-130">-ResourceGroupName</span></span>
<span data-ttu-id="388dc-131">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="388dc-131">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="388dc-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="388dc-132">-ResourceId</span></span>
<span data-ttu-id="388dc-133">Adjon meg egy fájlmegosztási erőforrás-azonosítót.</span><span class="sxs-lookup"><span data-stu-id="388dc-133">Input a File Share Resource Id.</span></span>

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

### <span data-ttu-id="388dc-134">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="388dc-134">-StorageAccount</span></span>
<span data-ttu-id="388dc-135">Storage Account objektum</span><span class="sxs-lookup"><span data-stu-id="388dc-135">Storage account object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount
Parameter Sets: AccountObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="388dc-136">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="388dc-136">-StorageAccountName</span></span>
<span data-ttu-id="388dc-137">Tárolási fiók neve.</span><span class="sxs-lookup"><span data-stu-id="388dc-137">Storage Account Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName
Aliases: AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="388dc-138">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="388dc-138">-Confirm</span></span>
<span data-ttu-id="388dc-139">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="388dc-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="388dc-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="388dc-140">-WhatIf</span></span>
<span data-ttu-id="388dc-141">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="388dc-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="388dc-142">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="388dc-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="388dc-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="388dc-143">CommonParameters</span></span>
<span data-ttu-id="388dc-144">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="388dc-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="388dc-145">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="388dc-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="388dc-146">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="388dc-146">INPUTS</span></span>

### <span data-ttu-id="388dc-147">System. String</span><span class="sxs-lookup"><span data-stu-id="388dc-147">System.String</span></span>

### <span data-ttu-id="388dc-148">Microsoft. Azure. Command. Management. Storage. models. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="388dc-148">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="388dc-149">Microsoft. Azure. Command. Management. Storage. models. PSShare</span><span class="sxs-lookup"><span data-stu-id="388dc-149">Microsoft.Azure.Commands.Management.Storage.Models.PSShare</span></span>

## <span data-ttu-id="388dc-150">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="388dc-150">OUTPUTS</span></span>

### <span data-ttu-id="388dc-151">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="388dc-151">System.Boolean</span></span>

## <span data-ttu-id="388dc-152">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="388dc-152">NOTES</span></span>

## <span data-ttu-id="388dc-153">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="388dc-153">RELATED LINKS</span></span>
