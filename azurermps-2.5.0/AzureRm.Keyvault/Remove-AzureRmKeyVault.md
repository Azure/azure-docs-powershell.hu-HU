---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 7A929BA8-02D9-4BBE-AFF3-B8781F8DDAD9
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/remove-azurermkeyvault
schema: 2.0.0
ms.openlocfilehash: 2365a58093be3193c7ac285d6dd38fbaf769ccd4
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93848209"
---
# <span data-ttu-id="480c4-101">Remove-AzureRmKeyVault</span><span class="sxs-lookup"><span data-stu-id="480c4-101">Remove-AzureRmKeyVault</span></span>

## <span data-ttu-id="480c4-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="480c4-102">SYNOPSIS</span></span>
<span data-ttu-id="480c4-103">Egy kulcs boltozatának törlése</span><span class="sxs-lookup"><span data-stu-id="480c4-103">Deletes a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="480c4-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="480c4-104">SYNTAX</span></span>

### <span data-ttu-id="480c4-105">ByAvailableVault</span><span class="sxs-lookup"><span data-stu-id="480c4-105">ByAvailableVault</span></span>
```
Remove-AzureRmKeyVault [-VaultName] <String> [[-ResourceGroupName] <String>] [[-Location] <String>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="480c4-106">ByDeletedVault</span><span class="sxs-lookup"><span data-stu-id="480c4-106">ByDeletedVault</span></span>
```
Remove-AzureRmKeyVault [-VaultName] <String> [-Location] <String> [-Force] [-InRemovedState] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="480c4-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="480c4-107">DESCRIPTION</span></span>
<span data-ttu-id="480c4-108">A **Remove-AzureRmKeyVault** parancsmag törli a megadott kulcs boltozatát.</span><span class="sxs-lookup"><span data-stu-id="480c4-108">The **Remove-AzureRmKeyVault** cmdlet deletes the specified key vault.</span></span>
<span data-ttu-id="480c4-109">Az adott példányban található összes kulcsot és titkot is törli.</span><span class="sxs-lookup"><span data-stu-id="480c4-109">It also deletes all keys and secrets contained in that instance.</span></span>

<span data-ttu-id="480c4-110">Fontos tudni, hogy az erőforráscsoport megadása esetén a parancsmag nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="480c4-110">Note that although specifying the resource group is optional for this cmdlet, you should so for better performance.</span></span>

## <span data-ttu-id="480c4-111">Példák</span><span class="sxs-lookup"><span data-stu-id="480c4-111">EXAMPLES</span></span>

### <span data-ttu-id="480c4-112">1. példa: kulcs-boltozat eltávolítása</span><span class="sxs-lookup"><span data-stu-id="480c4-112">Example 1: Remove a key vault</span></span>
```
PS C:\>Remove-AzureRmKeyVault -VaultName "Contoso03Vault"
```

<span data-ttu-id="480c4-113">Ez a parancs eltávolítja a Contoso03Vault nevű kulcs-boltozatot a jelenlegi előfizetésből.</span><span class="sxs-lookup"><span data-stu-id="480c4-113">This command removes the key vault named Contoso03Vault from your current subscription.</span></span>

### <span data-ttu-id="480c4-114">2. példa: kulcs-boltozat eltávolítása egy megadott erőforráscsoporthoz</span><span class="sxs-lookup"><span data-stu-id="480c4-114">Example 2: Remove a key vault from a specified resource group</span></span>
```
PS C:\>Remove-AzureRmKeyVault -VaultName "Contoso03Vault" -ResourceGroupName "Group14"
```

<span data-ttu-id="480c4-115">Ez a parancs eltávolítja a Contoso03Vault nevű kulcspárt a megnevezett erőforrás csoportból.</span><span class="sxs-lookup"><span data-stu-id="480c4-115">This command removes the key vault named Contoso03Vault from the named resource group.</span></span>
<span data-ttu-id="480c4-116">Ha nem adja meg az erőforráscsoport nevét, a parancsmag a megnevezett kulcs boltozatát keresi a jelenlegi előfizetésben.</span><span class="sxs-lookup"><span data-stu-id="480c4-116">If you do not specify the resource group name, the cmdlet searches for the named key vault to delete in your current subscription.</span></span>

## <span data-ttu-id="480c4-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="480c4-117">PARAMETERS</span></span>

### <span data-ttu-id="480c4-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="480c4-118">-AsJob</span></span>
<span data-ttu-id="480c4-119">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="480c4-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="480c4-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="480c4-120">-DefaultProfile</span></span>
<span data-ttu-id="480c4-121">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="480c4-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="480c4-122">-Force</span><span class="sxs-lookup"><span data-stu-id="480c4-122">-Force</span></span>
<span data-ttu-id="480c4-123">Azt jelzi, hogy a parancsmag nem kér megerősítést.</span><span class="sxs-lookup"><span data-stu-id="480c4-123">Indicates that the cmdlet does not prompt you for confirmation.</span></span>
<span data-ttu-id="480c4-124">Ez a parancsmag alapértelmezés szerint arra kéri, hogy erősítse meg, hogy törölni szeretné-e a kulcs boltozatát.</span><span class="sxs-lookup"><span data-stu-id="480c4-124">By default, this cmdlet prompts you to confirm that you want to delete the key vault.</span></span>

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

### <span data-ttu-id="480c4-125">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="480c4-125">-InRemovedState</span></span>
<span data-ttu-id="480c4-126">Törölje véglegesen a korábban törölt boltozatot.</span><span class="sxs-lookup"><span data-stu-id="480c4-126">Remove the previously deleted vault permanently.</span></span>

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

### <span data-ttu-id="480c4-127">-Hely</span><span class="sxs-lookup"><span data-stu-id="480c4-127">-Location</span></span>
<span data-ttu-id="480c4-128">A törölt boltozat helye.</span><span class="sxs-lookup"><span data-stu-id="480c4-128">The location of the deleted vault.</span></span>

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

### <span data-ttu-id="480c4-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="480c4-129">-ResourceGroupName</span></span>
<span data-ttu-id="480c4-130">Egy erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="480c4-130">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="480c4-131">-VaultName</span><span class="sxs-lookup"><span data-stu-id="480c4-131">-VaultName</span></span>
<span data-ttu-id="480c4-132">Az eltávolítandó kulcsfájl nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="480c4-132">Specifies the name of the key vault to remove.</span></span>

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

### <span data-ttu-id="480c4-133">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="480c4-133">-Confirm</span></span>
<span data-ttu-id="480c4-134">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="480c4-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="480c4-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="480c4-135">-WhatIf</span></span>
<span data-ttu-id="480c4-136">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="480c4-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="480c4-137">A parancsmag nem fut. Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="480c4-137">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="480c4-138">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="480c4-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="480c4-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="480c4-139">CommonParameters</span></span>
<span data-ttu-id="480c4-140">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="480c4-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="480c4-141">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="480c4-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="480c4-142">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="480c4-142">INPUTS</span></span>

## <span data-ttu-id="480c4-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="480c4-143">OUTPUTS</span></span>

## <span data-ttu-id="480c4-144">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="480c4-144">NOTES</span></span>

## <span data-ttu-id="480c4-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="480c4-145">RELATED LINKS</span></span>

[<span data-ttu-id="480c4-146">Get-AzureRmKeyVault</span><span class="sxs-lookup"><span data-stu-id="480c4-146">Get-AzureRmKeyVault</span></span>](./Get-AzureRmKeyVault.md)

[<span data-ttu-id="480c4-147">Új – AzureRmKeyVault</span><span class="sxs-lookup"><span data-stu-id="480c4-147">New-AzureRmKeyVault</span></span>](./New-AzureRmKeyVault.md)
