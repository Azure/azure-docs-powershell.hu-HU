---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 7A929BA8-02D9-4BBE-AFF3-B8781F8DDAD9
online version: https://docs.microsoft.com/en-us/powershell/module/Az.keyvault/remove-Azkeyvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Remove-AzKeyVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Remove-AzKeyVault.md
ms.openlocfilehash: 20187e2d7a844b472217fd30acbac9805e85ad40
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93843878"
---
# <span data-ttu-id="435e2-101">Remove-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="435e2-101">Remove-AzKeyVault</span></span>

## <span data-ttu-id="435e2-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="435e2-102">SYNOPSIS</span></span>
<span data-ttu-id="435e2-103">Egy kulcs boltozatának törlése</span><span class="sxs-lookup"><span data-stu-id="435e2-103">Deletes a key vault.</span></span>

## <span data-ttu-id="435e2-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="435e2-104">SYNTAX</span></span>

### <span data-ttu-id="435e2-105">ByAvailableVault</span><span class="sxs-lookup"><span data-stu-id="435e2-105">ByAvailableVault</span></span>
```
Remove-AzKeyVault [-VaultName] <String> [[-ResourceGroupName] <String>] [[-Location] <String>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="435e2-106">ByDeletedVault</span><span class="sxs-lookup"><span data-stu-id="435e2-106">ByDeletedVault</span></span>
```
Remove-AzKeyVault [-VaultName] <String> [-Location] <String> [-Force] [-InRemovedState] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="435e2-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="435e2-107">DESCRIPTION</span></span>
<span data-ttu-id="435e2-108">A **Remove-AzKeyVault** parancsmag törli a megadott kulcs boltozatát.</span><span class="sxs-lookup"><span data-stu-id="435e2-108">The **Remove-AzKeyVault** cmdlet deletes the specified key vault.</span></span>
<span data-ttu-id="435e2-109">Az adott példányban található összes kulcsot és titkot is törli.</span><span class="sxs-lookup"><span data-stu-id="435e2-109">It also deletes all keys and secrets contained in that instance.</span></span>

<span data-ttu-id="435e2-110">Fontos tudni, hogy az erőforráscsoport megadása esetén a parancsmag nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="435e2-110">Note that although specifying the resource group is optional for this cmdlet, you should so for better performance.</span></span>

## <span data-ttu-id="435e2-111">Példák</span><span class="sxs-lookup"><span data-stu-id="435e2-111">EXAMPLES</span></span>

### <span data-ttu-id="435e2-112">1. példa: kulcs-boltozat eltávolítása</span><span class="sxs-lookup"><span data-stu-id="435e2-112">Example 1: Remove a key vault</span></span>
```
PS C:\>Remove-AzKeyVault -VaultName "Contoso03Vault"
```

<span data-ttu-id="435e2-113">Ez a parancs eltávolítja a Contoso03Vault nevű kulcs-boltozatot a jelenlegi előfizetésből.</span><span class="sxs-lookup"><span data-stu-id="435e2-113">This command removes the key vault named Contoso03Vault from your current subscription.</span></span>

### <span data-ttu-id="435e2-114">2. példa: kulcs-boltozat eltávolítása egy megadott erőforráscsoporthoz</span><span class="sxs-lookup"><span data-stu-id="435e2-114">Example 2: Remove a key vault from a specified resource group</span></span>
```
PS C:\>Remove-AzKeyVault -VaultName "Contoso03Vault" -ResourceGroupName "Group14"
```

<span data-ttu-id="435e2-115">Ez a parancs eltávolítja a Contoso03Vault nevű kulcspárt a megnevezett erőforrás csoportból.</span><span class="sxs-lookup"><span data-stu-id="435e2-115">This command removes the key vault named Contoso03Vault from the named resource group.</span></span>
<span data-ttu-id="435e2-116">Ha nem adja meg az erőforráscsoport nevét, a parancsmag a megnevezett kulcs boltozatát keresi a jelenlegi előfizetésben.</span><span class="sxs-lookup"><span data-stu-id="435e2-116">If you do not specify the resource group name, the cmdlet searches for the named key vault to delete in your current subscription.</span></span>

## <span data-ttu-id="435e2-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="435e2-117">PARAMETERS</span></span>

### <span data-ttu-id="435e2-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="435e2-118">-AsJob</span></span>
<span data-ttu-id="435e2-119">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="435e2-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="435e2-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="435e2-120">-DefaultProfile</span></span>
<span data-ttu-id="435e2-121">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="435e2-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="435e2-122">-Force</span><span class="sxs-lookup"><span data-stu-id="435e2-122">-Force</span></span>
<span data-ttu-id="435e2-123">Azt jelzi, hogy a parancsmag nem kér megerősítést.</span><span class="sxs-lookup"><span data-stu-id="435e2-123">Indicates that the cmdlet does not prompt you for confirmation.</span></span>
<span data-ttu-id="435e2-124">Ez a parancsmag alapértelmezés szerint arra kéri, hogy erősítse meg, hogy törölni szeretné-e a kulcs boltozatát.</span><span class="sxs-lookup"><span data-stu-id="435e2-124">By default, this cmdlet prompts you to confirm that you want to delete the key vault.</span></span>

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

### <span data-ttu-id="435e2-125">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="435e2-125">-InRemovedState</span></span>
<span data-ttu-id="435e2-126">Törölje véglegesen a korábban törölt boltozatot.</span><span class="sxs-lookup"><span data-stu-id="435e2-126">Remove the previously deleted vault permanently.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ByDeletedVault
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="435e2-127">-Hely</span><span class="sxs-lookup"><span data-stu-id="435e2-127">-Location</span></span>
<span data-ttu-id="435e2-128">A törölt boltozat helye.</span><span class="sxs-lookup"><span data-stu-id="435e2-128">The location of the deleted vault.</span></span>

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

### <span data-ttu-id="435e2-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="435e2-129">-ResourceGroupName</span></span>
<span data-ttu-id="435e2-130">Egy erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="435e2-130">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="435e2-131">-VaultName</span><span class="sxs-lookup"><span data-stu-id="435e2-131">-VaultName</span></span>
<span data-ttu-id="435e2-132">Az eltávolítandó kulcsfájl nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="435e2-132">Specifies the name of the key vault to remove.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="435e2-133">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="435e2-133">-Confirm</span></span>
<span data-ttu-id="435e2-134">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="435e2-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="435e2-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="435e2-135">-WhatIf</span></span>
<span data-ttu-id="435e2-136">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="435e2-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="435e2-137">A parancsmag nem fut. Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="435e2-137">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="435e2-138">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="435e2-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="435e2-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="435e2-139">CommonParameters</span></span>
<span data-ttu-id="435e2-140">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="435e2-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="435e2-141">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="435e2-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="435e2-142">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="435e2-142">INPUTS</span></span>

### <span data-ttu-id="435e2-143">Nincs</span><span class="sxs-lookup"><span data-stu-id="435e2-143">None</span></span>
<span data-ttu-id="435e2-144">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="435e2-144">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="435e2-145">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="435e2-145">OUTPUTS</span></span>

## <span data-ttu-id="435e2-146">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="435e2-146">NOTES</span></span>

## <span data-ttu-id="435e2-147">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="435e2-147">RELATED LINKS</span></span>

[<span data-ttu-id="435e2-148">Get-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="435e2-148">Get-AzKeyVault</span></span>](./Get-AzKeyVault.md)

[<span data-ttu-id="435e2-149">Új – AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="435e2-149">New-AzKeyVault</span></span>](./New-AzKeyVault.md)
