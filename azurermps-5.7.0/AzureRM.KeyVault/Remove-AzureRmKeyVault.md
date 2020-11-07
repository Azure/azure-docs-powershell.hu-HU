---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 7A929BA8-02D9-4BBE-AFF3-B8781F8DDAD9
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/remove-azurermkeyvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureRmKeyVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureRmKeyVault.md
ms.openlocfilehash: 0c9e37433d28a16a28ca56daf4a726347b7a9533
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93672855"
---
# <span data-ttu-id="43149-101">Remove-AzureRmKeyVault</span><span class="sxs-lookup"><span data-stu-id="43149-101">Remove-AzureRmKeyVault</span></span>

## <span data-ttu-id="43149-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="43149-102">SYNOPSIS</span></span>
<span data-ttu-id="43149-103">Egy kulcs boltozatának törlése</span><span class="sxs-lookup"><span data-stu-id="43149-103">Deletes a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="43149-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="43149-104">SYNTAX</span></span>

### <span data-ttu-id="43149-105">ByAvailableVault (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="43149-105">ByAvailableVault (Default)</span></span>
```
Remove-AzureRmKeyVault [-VaultName] <String> [[-ResourceGroupName] <String>] [[-Location] <String>] [-Force]
 [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="43149-106">ByDeletedVault</span><span class="sxs-lookup"><span data-stu-id="43149-106">ByDeletedVault</span></span>
```
Remove-AzureRmKeyVault [-VaultName] <String> [-Location] <String> [-InRemovedState] [-Force] [-AsJob]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="43149-107">InputObjectByAvailableVault</span><span class="sxs-lookup"><span data-stu-id="43149-107">InputObjectByAvailableVault</span></span>
```
Remove-AzureRmKeyVault [-InputObject] <PSKeyVault> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="43149-108">InputObjectByDeletedVault</span><span class="sxs-lookup"><span data-stu-id="43149-108">InputObjectByDeletedVault</span></span>
```
Remove-AzureRmKeyVault [-InputObject] <PSKeyVault> [-InRemovedState] [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="43149-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="43149-109">DESCRIPTION</span></span>
<span data-ttu-id="43149-110">A **Remove-AzureRmKeyVault** parancsmag törli a megadott kulcs boltozatát.</span><span class="sxs-lookup"><span data-stu-id="43149-110">The **Remove-AzureRmKeyVault** cmdlet deletes the specified key vault.</span></span>
<span data-ttu-id="43149-111">Az adott példányban található összes kulcsot és titkot is törli.</span><span class="sxs-lookup"><span data-stu-id="43149-111">It also deletes all keys and secrets contained in that instance.</span></span>

<span data-ttu-id="43149-112">Fontos tudni, hogy az erőforráscsoport megadása esetén a parancsmag nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="43149-112">Note that although specifying the resource group is optional for this cmdlet, you should so for better performance.</span></span>

## <span data-ttu-id="43149-113">Példák</span><span class="sxs-lookup"><span data-stu-id="43149-113">EXAMPLES</span></span>

### <span data-ttu-id="43149-114">1. példa: kulcs-boltozat eltávolítása</span><span class="sxs-lookup"><span data-stu-id="43149-114">Example 1: Remove a key vault</span></span>
```
PS C:\>Remove-AzureRmKeyVault -VaultName "Contoso03Vault"
```

<span data-ttu-id="43149-115">Ez a parancs eltávolítja a Contoso03Vault nevű kulcs-boltozatot a jelenlegi előfizetésből.</span><span class="sxs-lookup"><span data-stu-id="43149-115">This command removes the key vault named Contoso03Vault from your current subscription.</span></span>

### <span data-ttu-id="43149-116">2. példa: kulcs-boltozat eltávolítása egy megadott erőforráscsoporthoz</span><span class="sxs-lookup"><span data-stu-id="43149-116">Example 2: Remove a key vault from a specified resource group</span></span>
```
PS C:\>Remove-AzureRmKeyVault -VaultName "Contoso03Vault" -ResourceGroupName "Group14"
```

<span data-ttu-id="43149-117">Ez a parancs eltávolítja a Contoso03Vault nevű kulcspárt a megnevezett erőforrás csoportból.</span><span class="sxs-lookup"><span data-stu-id="43149-117">This command removes the key vault named Contoso03Vault from the named resource group.</span></span>
<span data-ttu-id="43149-118">Ha nem adja meg az erőforráscsoport nevét, a parancsmag a megnevezett kulcs boltozatát keresi a jelenlegi előfizetésben.</span><span class="sxs-lookup"><span data-stu-id="43149-118">If you do not specify the resource group name, the cmdlet searches for the named key vault to delete in your current subscription.</span></span>

## <span data-ttu-id="43149-119">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="43149-119">PARAMETERS</span></span>

### <span data-ttu-id="43149-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="43149-120">-AsJob</span></span>
<span data-ttu-id="43149-121">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="43149-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="43149-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="43149-122">-DefaultProfile</span></span>
<span data-ttu-id="43149-123">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="43149-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="43149-124">-Force</span><span class="sxs-lookup"><span data-stu-id="43149-124">-Force</span></span>
<span data-ttu-id="43149-125">Azt jelzi, hogy a parancsmag nem kér megerősítést.</span><span class="sxs-lookup"><span data-stu-id="43149-125">Indicates that the cmdlet does not prompt you for confirmation.</span></span>
<span data-ttu-id="43149-126">Ez a parancsmag alapértelmezés szerint arra kéri, hogy erősítse meg, hogy törölni szeretné-e a kulcs boltozatát.</span><span class="sxs-lookup"><span data-stu-id="43149-126">By default, this cmdlet prompts you to confirm that you want to delete the key vault.</span></span>

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

### <span data-ttu-id="43149-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="43149-127">-InputObject</span></span>
<span data-ttu-id="43149-128">A kulcsfájl törlésére szolgáló objektum.</span><span class="sxs-lookup"><span data-stu-id="43149-128">Key Vault object to be deleted.</span></span>

```yaml
Type: PSKeyVault
Parameter Sets: InputObjectByAvailableVault, InputObjectByDeletedVault
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="43149-129">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="43149-129">-InRemovedState</span></span>
<span data-ttu-id="43149-130">Törölje véglegesen a korábban törölt boltozatot.</span><span class="sxs-lookup"><span data-stu-id="43149-130">Remove the previously deleted vault permanently.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ByDeletedVault, InputObjectByDeletedVault
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="43149-131">-Hely</span><span class="sxs-lookup"><span data-stu-id="43149-131">-Location</span></span>
<span data-ttu-id="43149-132">A törölt boltozat helye.</span><span class="sxs-lookup"><span data-stu-id="43149-132">The location of the deleted vault.</span></span>

```yaml
Type: String
Parameter Sets: ByAvailableVault
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ByDeletedVault
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="43149-133">-PassThru</span><span class="sxs-lookup"><span data-stu-id="43149-133">-PassThru</span></span>
<span data-ttu-id="43149-134">Ez a parancsmag alapértelmezés szerint nem ad vissza objektumot.</span><span class="sxs-lookup"><span data-stu-id="43149-134">This Cmdlet does not return an object by default.</span></span> <span data-ttu-id="43149-135">Ha meg van adva ez a kapcsoló, az eredmény igaz, ha sikeres.</span><span class="sxs-lookup"><span data-stu-id="43149-135">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="43149-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="43149-136">-ResourceGroupName</span></span>
<span data-ttu-id="43149-137">Egy erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="43149-137">Specifies the name of a resource group.</span></span>

```yaml
Type: String
Parameter Sets: ByAvailableVault
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="43149-138">-VaultName</span><span class="sxs-lookup"><span data-stu-id="43149-138">-VaultName</span></span>
<span data-ttu-id="43149-139">Az eltávolítandó kulcsfájl nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="43149-139">Specifies the name of the key vault to remove.</span></span>

```yaml
Type: String
Parameter Sets: ByAvailableVault, ByDeletedVault
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="43149-140">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="43149-140">-Confirm</span></span>
<span data-ttu-id="43149-141">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="43149-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="43149-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="43149-142">-WhatIf</span></span>
<span data-ttu-id="43149-143">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="43149-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="43149-144">A parancsmag nem fut. Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="43149-144">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="43149-145">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="43149-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="43149-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="43149-146">CommonParameters</span></span>
<span data-ttu-id="43149-147">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="43149-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="43149-148">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="43149-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="43149-149">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="43149-149">INPUTS</span></span>

### <span data-ttu-id="43149-150">Nincs</span><span class="sxs-lookup"><span data-stu-id="43149-150">None</span></span>
<span data-ttu-id="43149-151">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="43149-151">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="43149-152">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="43149-152">OUTPUTS</span></span>

### <span data-ttu-id="43149-153">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="43149-153">System.Boolean</span></span>

## <span data-ttu-id="43149-154">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="43149-154">NOTES</span></span>

## <span data-ttu-id="43149-155">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="43149-155">RELATED LINKS</span></span>

[<span data-ttu-id="43149-156">Get-AzureRmKeyVault</span><span class="sxs-lookup"><span data-stu-id="43149-156">Get-AzureRmKeyVault</span></span>](./Get-AzureRmKeyVault.md)

[<span data-ttu-id="43149-157">Új – AzureRmKeyVault</span><span class="sxs-lookup"><span data-stu-id="43149-157">New-AzureRmKeyVault</span></span>](./New-AzureRmKeyVault.md)
