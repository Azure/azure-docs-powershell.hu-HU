---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 7A929BA8-02D9-4BBE-AFF3-B8781F8DDAD9
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/remove-azurermkeyvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureRmKeyVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureRmKeyVault.md
ms.openlocfilehash: c91bc951ef06f2e591893f0959120cac3700b070
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93496051"
---
# <span data-ttu-id="9567e-101">Remove-AzureRmKeyVault</span><span class="sxs-lookup"><span data-stu-id="9567e-101">Remove-AzureRmKeyVault</span></span>

## <span data-ttu-id="9567e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="9567e-102">SYNOPSIS</span></span>
<span data-ttu-id="9567e-103">Egy kulcs boltozatának törlése</span><span class="sxs-lookup"><span data-stu-id="9567e-103">Deletes a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9567e-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="9567e-104">SYNTAX</span></span>

### <span data-ttu-id="9567e-105">ByAvailableVault (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="9567e-105">ByAvailableVault (Default)</span></span>
```
Remove-AzureRmKeyVault [-VaultName] <String> [[-ResourceGroupName] <String>] [[-Location] <String>] [-Force]
 [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9567e-106">ByDeletedVault</span><span class="sxs-lookup"><span data-stu-id="9567e-106">ByDeletedVault</span></span>
```
Remove-AzureRmKeyVault [-VaultName] <String> [-Location] <String> [-InRemovedState] [-Force] [-AsJob]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9567e-107">InputObjectByAvailableVault</span><span class="sxs-lookup"><span data-stu-id="9567e-107">InputObjectByAvailableVault</span></span>
```
Remove-AzureRmKeyVault [-InputObject] <PSKeyVault> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9567e-108">InputObjectByDeletedVault</span><span class="sxs-lookup"><span data-stu-id="9567e-108">InputObjectByDeletedVault</span></span>
```
Remove-AzureRmKeyVault [-InputObject] <PSKeyVault> [-InRemovedState] [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9567e-109">ResourceIdByAvailableVault</span><span class="sxs-lookup"><span data-stu-id="9567e-109">ResourceIdByAvailableVault</span></span>
```
Remove-AzureRmKeyVault [-ResourceId] <String> [[-Location] <String>] [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9567e-110">ResourceIdByDeletedVault</span><span class="sxs-lookup"><span data-stu-id="9567e-110">ResourceIdByDeletedVault</span></span>
```
Remove-AzureRmKeyVault [-ResourceId] <String> [-Location] <String> [-InRemovedState] [-Force] [-AsJob]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9567e-111">Leírás</span><span class="sxs-lookup"><span data-stu-id="9567e-111">DESCRIPTION</span></span>
<span data-ttu-id="9567e-112">A **Remove-AzureRmKeyVault** parancsmag törli a megadott kulcs boltozatát.</span><span class="sxs-lookup"><span data-stu-id="9567e-112">The **Remove-AzureRmKeyVault** cmdlet deletes the specified key vault.</span></span>
<span data-ttu-id="9567e-113">Az adott példányban található összes kulcsot és titkot is törli.</span><span class="sxs-lookup"><span data-stu-id="9567e-113">It also deletes all keys and secrets contained in that instance.</span></span>
<span data-ttu-id="9567e-114">Fontos tudni, hogy az erőforráscsoport megadása esetén a parancsmag nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="9567e-114">Note that although specifying the resource group is optional for this cmdlet, you should so for better performance.</span></span>

## <span data-ttu-id="9567e-115">Példák</span><span class="sxs-lookup"><span data-stu-id="9567e-115">EXAMPLES</span></span>

### <span data-ttu-id="9567e-116">1. példa: kulcs-boltozat eltávolítása</span><span class="sxs-lookup"><span data-stu-id="9567e-116">Example 1: Remove a key vault</span></span>
```powershell
PS C:\> Remove-AzureRmKeyVault -VaultName "Contoso03Vault" -PassThru

True
```

<span data-ttu-id="9567e-117">Ez a parancs eltávolítja a Contoso03Vault nevű kulcs-boltozatot a jelenlegi előfizetésből.</span><span class="sxs-lookup"><span data-stu-id="9567e-117">This command removes the key vault named Contoso03Vault from your current subscription.</span></span>

### <span data-ttu-id="9567e-118">2. példa: kulcs-boltozat eltávolítása egy megadott erőforráscsoporthoz</span><span class="sxs-lookup"><span data-stu-id="9567e-118">Example 2: Remove a key vault from a specified resource group</span></span>
```powershell
PS C:\> Remove-AzureRmKeyVault -VaultName "Contoso03Vault" -ResourceGroupName "Group14" -PassThru

True
```

<span data-ttu-id="9567e-119">Ez a parancs eltávolítja a Contoso03Vault nevű kulcspárt a megnevezett erőforrás csoportból.</span><span class="sxs-lookup"><span data-stu-id="9567e-119">This command removes the key vault named Contoso03Vault from the named resource group.</span></span>
<span data-ttu-id="9567e-120">Ha nem adja meg az erőforráscsoport nevét, a parancsmag a megnevezett kulcs boltozatát keresi a jelenlegi előfizetésben.</span><span class="sxs-lookup"><span data-stu-id="9567e-120">If you do not specify the resource group name, the cmdlet searches for the named key vault to delete in your current subscription.</span></span>

## <span data-ttu-id="9567e-121">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="9567e-121">PARAMETERS</span></span>

### <span data-ttu-id="9567e-122">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9567e-122">-AsJob</span></span>
<span data-ttu-id="9567e-123">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="9567e-123">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9567e-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9567e-124">-DefaultProfile</span></span>
<span data-ttu-id="9567e-125">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="9567e-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9567e-126">-Force</span><span class="sxs-lookup"><span data-stu-id="9567e-126">-Force</span></span>
<span data-ttu-id="9567e-127">Azt jelzi, hogy a parancsmag nem kér megerősítést.</span><span class="sxs-lookup"><span data-stu-id="9567e-127">Indicates that the cmdlet does not prompt you for confirmation.</span></span>
<span data-ttu-id="9567e-128">Ez a parancsmag alapértelmezés szerint arra kéri, hogy erősítse meg, hogy törölni szeretné-e a kulcs boltozatát.</span><span class="sxs-lookup"><span data-stu-id="9567e-128">By default, this cmdlet prompts you to confirm that you want to delete the key vault.</span></span>

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

### <span data-ttu-id="9567e-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9567e-129">-InputObject</span></span>
<span data-ttu-id="9567e-130">A kulcsfájl törlésére szolgáló objektum.</span><span class="sxs-lookup"><span data-stu-id="9567e-130">Key Vault object to be deleted.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault
Parameter Sets: InputObjectByAvailableVault, InputObjectByDeletedVault
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9567e-131">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="9567e-131">-InRemovedState</span></span>
<span data-ttu-id="9567e-132">Törölje véglegesen a korábban törölt boltozatot.</span><span class="sxs-lookup"><span data-stu-id="9567e-132">Remove the previously deleted vault permanently.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByDeletedVault, InputObjectByDeletedVault, ResourceIdByDeletedVault
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9567e-133">-Hely</span><span class="sxs-lookup"><span data-stu-id="9567e-133">-Location</span></span>
<span data-ttu-id="9567e-134">A törölt boltozat helye.</span><span class="sxs-lookup"><span data-stu-id="9567e-134">The location of the deleted vault.</span></span>

```yaml
Type: System.String
Parameter Sets: ByAvailableVault, ResourceIdByAvailableVault
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByDeletedVault, ResourceIdByDeletedVault
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9567e-135">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9567e-135">-PassThru</span></span>
<span data-ttu-id="9567e-136">Ez a parancsmag alapértelmezés szerint nem ad vissza objektumot.</span><span class="sxs-lookup"><span data-stu-id="9567e-136">This Cmdlet does not return an object by default.</span></span> <span data-ttu-id="9567e-137">Ha meg van adva ez a kapcsoló, az eredmény igaz, ha sikeres.</span><span class="sxs-lookup"><span data-stu-id="9567e-137">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="9567e-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9567e-138">-ResourceGroupName</span></span>
<span data-ttu-id="9567e-139">Egy erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="9567e-139">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ByAvailableVault
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9567e-140">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9567e-140">-ResourceId</span></span>
<span data-ttu-id="9567e-141">A főkészlet erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="9567e-141">KeyVault Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdByAvailableVault, ResourceIdByDeletedVault
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9567e-142">-VaultName</span><span class="sxs-lookup"><span data-stu-id="9567e-142">-VaultName</span></span>
<span data-ttu-id="9567e-143">Az eltávolítandó kulcsfájl nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="9567e-143">Specifies the name of the key vault to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: ByAvailableVault, ByDeletedVault
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9567e-144">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="9567e-144">-Confirm</span></span>
<span data-ttu-id="9567e-145">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="9567e-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9567e-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9567e-146">-WhatIf</span></span>
<span data-ttu-id="9567e-147">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="9567e-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9567e-148">A parancsmag nem fut. Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="9567e-148">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9567e-149">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="9567e-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9567e-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9567e-150">CommonParameters</span></span>
<span data-ttu-id="9567e-151">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="9567e-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9567e-152">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9567e-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9567e-153">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="9567e-153">INPUTS</span></span>

### <span data-ttu-id="9567e-154">Microsoft. Azure. Command. PSKeyVault. models.</span><span class="sxs-lookup"><span data-stu-id="9567e-154">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>
<span data-ttu-id="9567e-155">Paraméterek: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="9567e-155">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="9567e-156">System. String</span><span class="sxs-lookup"><span data-stu-id="9567e-156">System.String</span></span>

## <span data-ttu-id="9567e-157">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9567e-157">OUTPUTS</span></span>

### <span data-ttu-id="9567e-158">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="9567e-158">System.Boolean</span></span>

## <span data-ttu-id="9567e-159">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="9567e-159">NOTES</span></span>

## <span data-ttu-id="9567e-160">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9567e-160">RELATED LINKS</span></span>

[<span data-ttu-id="9567e-161">Get-AzureRmKeyVault</span><span class="sxs-lookup"><span data-stu-id="9567e-161">Get-AzureRmKeyVault</span></span>](./Get-AzureRmKeyVault.md)

[<span data-ttu-id="9567e-162">Új – AzureRmKeyVault</span><span class="sxs-lookup"><span data-stu-id="9567e-162">New-AzureRmKeyVault</span></span>](./New-AzureRmKeyVault.md)
