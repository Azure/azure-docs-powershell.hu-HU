---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/set-azrmstoragecontainerimmutabilitypolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzRmStorageContainerImmutabilityPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzRmStorageContainerImmutabilityPolicy.md
ms.openlocfilehash: 9631855803b4ad16312c907c1d1c747b3aee6fdf
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98348330"
---
# <span data-ttu-id="5f282-101">Set-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="5f282-101">Set-AzRmStorageContainerImmutabilityPolicy</span></span>

## <span data-ttu-id="5f282-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5f282-102">SYNOPSIS</span></span>
<span data-ttu-id="5f282-103">Tárterület blobtárolói ImmutabilityPolicy-ját hozza létre vagy frissíti.</span><span class="sxs-lookup"><span data-stu-id="5f282-103">Creates or updates ImmutabilityPolicy of a Storage blob containers</span></span>

## <span data-ttu-id="5f282-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="5f282-104">SYNTAX</span></span>

### <span data-ttu-id="5f282-105">AccountName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="5f282-105">AccountName (Default)</span></span>
```
Set-AzRmStorageContainerImmutabilityPolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 -ContainerName <String> [-ImmutabilityPeriod <Int32>] [-AllowProtectedAppendWrite <Boolean>] [-Etag <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5f282-106">ExtendAccountName</span><span class="sxs-lookup"><span data-stu-id="5f282-106">ExtendAccountName</span></span>
```
Set-AzRmStorageContainerImmutabilityPolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 -ContainerName <String> -ImmutabilityPeriod <Int32> -Etag <String> [-ExtendPolicy]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5f282-107">AccountObject</span><span class="sxs-lookup"><span data-stu-id="5f282-107">AccountObject</span></span>
```
Set-AzRmStorageContainerImmutabilityPolicy -ContainerName <String> -StorageAccount <PSStorageAccount>
 [-ImmutabilityPeriod <Int32>] [-AllowProtectedAppendWrite <Boolean>] [-Etag <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5f282-108">ExtendAccountObject</span><span class="sxs-lookup"><span data-stu-id="5f282-108">ExtendAccountObject</span></span>
```
Set-AzRmStorageContainerImmutabilityPolicy -ContainerName <String> -StorageAccount <PSStorageAccount>
 -ImmutabilityPeriod <Int32> -Etag <String> [-ExtendPolicy] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5f282-109">ContainerObject</span><span class="sxs-lookup"><span data-stu-id="5f282-109">ContainerObject</span></span>
```
Set-AzRmStorageContainerImmutabilityPolicy -Container <PSContainer> [-ImmutabilityPeriod <Int32>]
 [-AllowProtectedAppendWrite <Boolean>] [-Etag <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5f282-110">ExtendContainerObject</span><span class="sxs-lookup"><span data-stu-id="5f282-110">ExtendContainerObject</span></span>
```
Set-AzRmStorageContainerImmutabilityPolicy -Container <PSContainer> -ImmutabilityPeriod <Int32> -Etag <String>
 [-ExtendPolicy] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5f282-111">ImmutabilityPolicyObject</span><span class="sxs-lookup"><span data-stu-id="5f282-111">ImmutabilityPolicyObject</span></span>
```
Set-AzRmStorageContainerImmutabilityPolicy [-InputObject] <PSImmutabilityPolicy> [-ImmutabilityPeriod <Int32>]
 [-AllowProtectedAppendWrite <Boolean>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5f282-112">ExtendImmutabilityPolicyObject</span><span class="sxs-lookup"><span data-stu-id="5f282-112">ExtendImmutabilityPolicyObject</span></span>
```
Set-AzRmStorageContainerImmutabilityPolicy [-InputObject] <PSImmutabilityPolicy> -ImmutabilityPeriod <Int32>
 [-ExtendPolicy] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5f282-113">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="5f282-113">DESCRIPTION</span></span>
<span data-ttu-id="5f282-114">A **Set-AzRmStorageContainerImmutabilityPolicy parancsmag** létrehoz vagy frissítéseket hoz létre vagy frissítéseket hoz létre egy tároló blobtárolójában.</span><span class="sxs-lookup"><span data-stu-id="5f282-114">The **Set-AzRmStorageContainerImmutabilityPolicy** cmdlet creates or updates ImmutabilityPolicy of a Storage blob containers</span></span>

## <span data-ttu-id="5f282-115">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="5f282-115">EXAMPLES</span></span>

### <span data-ttu-id="5f282-116">1. példa: Tárfiók nevét és tárolónevét tartalmazó tár blobtároló ImmutabilityPolicy-ának létrehozása vagy frissítése</span><span class="sxs-lookup"><span data-stu-id="5f282-116">Example 1: Create or update ImmutabilityPolicy of a Storage blob container with Storage account name and container name</span></span>
```
PS C:\>Set-AzRmStorageContainerImmutabilityPolicy -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer" -ImmutabilityPeriod 10
```

<span data-ttu-id="5f282-117">Ez a parancs létrehozza vagy frissíti egy Tároló blobtároló ImmutabilityPolicy fájlját tárfióknévvel és tárolónévvel.</span><span class="sxs-lookup"><span data-stu-id="5f282-117">This command creates or updates ImmutabilityPolicy of a Storage blob container with Storage account name and container name.</span></span>

### <span data-ttu-id="5f282-118">2. példa: Tárterület blobtároló ImmutabilityPolicy-ának kiterjesztése Tárfiók-objektummal</span><span class="sxs-lookup"><span data-stu-id="5f282-118">Example 2: Extend ImmutabilityPolicy of a Storage blob container, with Storage account object</span></span>
```
PS C:\>$accountObject = Get-AzStorageAccount -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
PS C:\>$policy = Get-AzRmStorageContainerImmutabilityPolicy -StorageAccount $accountObject -ContainerName "myContainer"
PS C:\>Set-AzRmStorageContainerImmutabilityPolicy -StorageAccount $accountObject -ContainerName "myContainer" -ImmutabilityPeriod 20 -Etag $policy.Etag -ExtendPolicy
```

<span data-ttu-id="5f282-119">Ez a parancs kibővíti a Tárterület blobtároló ImmutabilityPolicy parancsát a Tárfiók objektummal.</span><span class="sxs-lookup"><span data-stu-id="5f282-119">This command extend ImmutabilityPolicy of a Storage blob container, with Storage account object.</span></span> <span data-ttu-id="5f282-120">A ImmutabilityPolicy kiterjesztés csak akkor futtatható, ha a ImmutabilityPolicy zárolva van.</span><span class="sxs-lookup"><span data-stu-id="5f282-120">Extend ImmutabilityPolicy can only run after ImmutabilityPolicy is locked.</span></span>

### <span data-ttu-id="5f282-121">3. példa: A Tárterület blobtároló ImmutabilityPolicy-ának frissítése</span><span class="sxs-lookup"><span data-stu-id="5f282-121">Example 3: Update ImmutabilityPolicy of a Storage blob container</span></span>
```
PS C:\>$containerObject = Get-AzStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -Name "myContainer"
PS C:\>$policy = Set-AzRmStorageContainerImmutabilityPolicy -Container $containerObject -ImmutabilityPeriod 12
PS C:\>$policy = Set-AzRmStorageContainerImmutabilityPolicy -Container $containerObject -ImmutabilityPeriod 9 -Etag $policy.Etag
PS C:\>$policy = Set-AzRmStorageContainerImmutabilityPolicy -Container $containerObject -AllowProtectedAppendWrite $true
```

<span data-ttu-id="5f282-122">Ez a parancs 3 alkalommal frissíti egy Tároló blobtároló ImmutabilityPolicy funkcióját Tárolótároló objektummal: Először a ImmutabilityPeriod 12 nappal etag nélkül, majd a ImmutabilityPeriod 9 nap etaggal, végül az AllowProtectedAppendWrite engedélyezése.</span><span class="sxs-lookup"><span data-stu-id="5f282-122">This command updates ImmutabilityPolicy of a Storage blob container with Storage container object 3 times: First to ImmutabilityPeriod 12 days without etag, then to ImmutabilityPeriod 9 days with etag, finally enabled AllowProtectedAppendWrite.</span></span>

### <span data-ttu-id="5f282-123">4. példa: Tárterület blobtároló ImmutabilityPolicy-ának kiterjesztése ImmutabilityPolicy objektummal</span><span class="sxs-lookup"><span data-stu-id="5f282-123">Example 4: Extend ImmutabilityPolicy of a Storage blob container, with ImmutabilityPolicy object</span></span>
```
PS C:\>Get-AzRmStorageContainerImmutabilityPolicy -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer" | Set-AzRmStorageContainerImmutabilityPolicy -ImmutabilityPeriod 15 -ExtendPolicy
```

<span data-ttu-id="5f282-124">Ezzel a paranccsal kiterjesztheti egy Tároló blobtároló ImmutabilityPolicy parancsát, ImmutabilityPolicy objektummal.</span><span class="sxs-lookup"><span data-stu-id="5f282-124">This command extend ImmutabilityPolicy of a Storage blob container, with ImmutabilityPolicy object.</span></span> <span data-ttu-id="5f282-125">A ImmutabilityPolicy kiterjesztés csak akkor futtatható, ha a ImmutabilityPolicy zárolva van.</span><span class="sxs-lookup"><span data-stu-id="5f282-125">Extend ImmutabilityPolicy can only run after ImmutabilityPolicy is locked.</span></span>

## <span data-ttu-id="5f282-126">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5f282-126">PARAMETERS</span></span>

### <span data-ttu-id="5f282-127">-AllowProtectedAppendWrite</span><span class="sxs-lookup"><span data-stu-id="5f282-127">-AllowProtectedAppendWrite</span></span>
<span data-ttu-id="5f282-128">Ez a tulajdonság csak zárolt időalapú adatmegőrzési házirendek esetén módosítható.</span><span class="sxs-lookup"><span data-stu-id="5f282-128">This property can only be changed for unlocked time-based retention policies.</span></span> <span data-ttu-id="5f282-129">Ha ez a tulajdonság engedélyezve van, új blokkok írhatóak hozzáfűző blobba úgy, hogy közben megőrizze a inmutbilitás védelmét és a megfelelőséget.</span><span class="sxs-lookup"><span data-stu-id="5f282-129">With this property enabled, new blocks can be written to an append blob while maintaining immutability protection and compliance.</span></span> <span data-ttu-id="5f282-130">Csak új blokkokat lehet hozzáadni, a meglévő blokkokat pedig nem lehet módosítani vagy törölni.</span><span class="sxs-lookup"><span data-stu-id="5f282-130">Only new blocks can be added and any existing blocks cannot be modified or deleted.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: AccountName, AccountObject, ContainerObject, ImmutabilityPolicyObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5f282-131">-Container</span><span class="sxs-lookup"><span data-stu-id="5f282-131">-Container</span></span>
<span data-ttu-id="5f282-132">Tárolóobjektum</span><span class="sxs-lookup"><span data-stu-id="5f282-132">Storage container object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSContainer
Parameter Sets: ContainerObject, ExtendContainerObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5f282-133">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="5f282-133">-ContainerName</span></span>
<span data-ttu-id="5f282-134">Tároló neve</span><span class="sxs-lookup"><span data-stu-id="5f282-134">Container Name</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName, ExtendAccountName, AccountObject, ExtendAccountObject
Aliases: N

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5f282-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5f282-135">-DefaultProfile</span></span>
<span data-ttu-id="5f282-136">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="5f282-136">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5f282-137">-Etag</span><span class="sxs-lookup"><span data-stu-id="5f282-137">-Etag</span></span>
<span data-ttu-id="5f282-138">Immutability policy etag.</span><span class="sxs-lookup"><span data-stu-id="5f282-138">Immutability policy etag.</span></span> <span data-ttu-id="5f282-139">Ha az -ExtendPolicy nincs megadva, az Etag megadása nem kötelező; else Etag is required.</span><span class="sxs-lookup"><span data-stu-id="5f282-139">If -ExtendPolicy is not specified, Etag is optional; else Etag is required.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName, AccountObject, ContainerObject
Aliases: IfMatch

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ExtendAccountName, ExtendAccountObject, ExtendContainerObject
Aliases: IfMatch

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5f282-140">-ExtendPolicy</span><span class="sxs-lookup"><span data-stu-id="5f282-140">-ExtendPolicy</span></span>
<span data-ttu-id="5f282-141">Az ExtendPolicy jelzése meglévő ImmutabilityPolicy kiterjesztésre</span><span class="sxs-lookup"><span data-stu-id="5f282-141">Indicate ExtendPolicy to Extend an existing ImmutabilityPolicy.</span></span>  <span data-ttu-id="5f282-142">A ImmutabilityPolicy zárolt, de csak akkor hosszabbítható meg.</span><span class="sxs-lookup"><span data-stu-id="5f282-142">After ImmutabilityPolicy is locked, it can only be extend.</span></span> 

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ExtendAccountName, ExtendAccountObject, ExtendContainerObject, ExtendImmutabilityPolicyObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5f282-143">-ImmutabilityPeriod</span><span class="sxs-lookup"><span data-stu-id="5f282-143">-ImmutabilityPeriod</span></span>
<span data-ttu-id="5f282-144">Napok óta nem módosítható az időtartomány a létrehozás óta.</span><span class="sxs-lookup"><span data-stu-id="5f282-144">Immutability period since creation in days.</span></span>

```yaml
Type: System.Int32
Parameter Sets: AccountName, AccountObject, ContainerObject, ImmutabilityPolicyObject
Aliases: ImmutabilityPeriodSinceCreationInDays

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.Int32
Parameter Sets: ExtendAccountName, ExtendAccountObject, ExtendContainerObject, ExtendImmutabilityPolicyObject
Aliases: ImmutabilityPeriodSinceCreationInDays

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5f282-145">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5f282-145">-InputObject</span></span>
<span data-ttu-id="5f282-146">Tároló neve</span><span class="sxs-lookup"><span data-stu-id="5f282-146">Container Name</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSImmutabilityPolicy
Parameter Sets: ImmutabilityPolicyObject, ExtendImmutabilityPolicyObject
Aliases: ImmutabilityPolicy

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5f282-147">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5f282-147">-ResourceGroupName</span></span>
<span data-ttu-id="5f282-148">Erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="5f282-148">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName, ExtendAccountName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5f282-149">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="5f282-149">-StorageAccount</span></span>
<span data-ttu-id="5f282-150">Tárfiók objektum</span><span class="sxs-lookup"><span data-stu-id="5f282-150">Storage account object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount
Parameter Sets: AccountObject, ExtendAccountObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5f282-151">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="5f282-151">-StorageAccountName</span></span>
<span data-ttu-id="5f282-152">Tárfiók neve.</span><span class="sxs-lookup"><span data-stu-id="5f282-152">Storage Account Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName, ExtendAccountName
Aliases: AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5f282-153">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5f282-153">-Confirm</span></span>
<span data-ttu-id="5f282-154">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="5f282-154">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5f282-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5f282-155">-WhatIf</span></span>
<span data-ttu-id="5f282-156">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="5f282-156">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5f282-157">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="5f282-157">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5f282-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5f282-158">CommonParameters</span></span>
<span data-ttu-id="5f282-159">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5f282-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5f282-160">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5f282-160">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5f282-161">INPUTS</span><span class="sxs-lookup"><span data-stu-id="5f282-161">INPUTS</span></span>

### <span data-ttu-id="5f282-162">System.String</span><span class="sxs-lookup"><span data-stu-id="5f282-162">System.String</span></span>

### <span data-ttu-id="5f282-163">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="5f282-163">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="5f282-164">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span><span class="sxs-lookup"><span data-stu-id="5f282-164">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span></span>

### <span data-ttu-id="5f282-165">Microsoft.Azure.Commands.Management.Storage.Models.PSImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="5f282-165">Microsoft.Azure.Commands.Management.Storage.Models.PSImmutabilityPolicy</span></span>

## <span data-ttu-id="5f282-166">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5f282-166">OUTPUTS</span></span>

### <span data-ttu-id="5f282-167">Microsoft.Azure.Commands.Management.Storage.Models.PSImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="5f282-167">Microsoft.Azure.Commands.Management.Storage.Models.PSImmutabilityPolicy</span></span>

## <span data-ttu-id="5f282-168">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="5f282-168">NOTES</span></span>

## <span data-ttu-id="5f282-169">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5f282-169">RELATED LINKS</span></span>
