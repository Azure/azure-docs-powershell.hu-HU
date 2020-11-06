---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 7A929BA8-02D9-4BBE-AFF3-B8781F8DDAD9
online version: https://go.microsoft.com/fwlink/?LinkId=690162
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureRmKeyVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureRmKeyVault.md
ms.openlocfilehash: 2a30a190fbf257142e1c1e4fb4329fd6c4f41e3d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93502696"
---
# <span data-ttu-id="f839a-101">Remove-AzureRmKeyVault</span><span class="sxs-lookup"><span data-stu-id="f839a-101">Remove-AzureRmKeyVault</span></span>

## <span data-ttu-id="f839a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f839a-102">SYNOPSIS</span></span>
<span data-ttu-id="f839a-103">Egy kulcs boltozatának törlése</span><span class="sxs-lookup"><span data-stu-id="f839a-103">Deletes a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f839a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f839a-104">SYNTAX</span></span>

### <span data-ttu-id="f839a-105">ByAvailableVault</span><span class="sxs-lookup"><span data-stu-id="f839a-105">ByAvailableVault</span></span>
```
Remove-AzureRmKeyVault [-VaultName] <String> [[-ResourceGroupName] <String>] [[-Location] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f839a-106">ByDeletedVault</span><span class="sxs-lookup"><span data-stu-id="f839a-106">ByDeletedVault</span></span>
```
Remove-AzureRmKeyVault [-VaultName] <String> [-Location] <String> [-Force] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f839a-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="f839a-107">DESCRIPTION</span></span>
<span data-ttu-id="f839a-108">A **Remove-AzureRmKeyVault** parancsmag törli a megadott kulcs boltozatát.</span><span class="sxs-lookup"><span data-stu-id="f839a-108">The **Remove-AzureRmKeyVault** cmdlet deletes the specified key vault.</span></span>
<span data-ttu-id="f839a-109">Az adott példányban található összes kulcsot és titkot is törli.</span><span class="sxs-lookup"><span data-stu-id="f839a-109">It also deletes all keys and secrets contained in that instance.</span></span>

<span data-ttu-id="f839a-110">Fontos tudni, hogy az erőforráscsoport megadása esetén a parancsmag nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="f839a-110">Note that although specifying the resource group is optional for this cmdlet, you should so for better performance.</span></span>

## <span data-ttu-id="f839a-111">Példák</span><span class="sxs-lookup"><span data-stu-id="f839a-111">EXAMPLES</span></span>

### <span data-ttu-id="f839a-112">1. példa: kulcs-boltozat eltávolítása</span><span class="sxs-lookup"><span data-stu-id="f839a-112">Example 1: Remove a key vault</span></span>
```
PS C:\>Remove-AzureRmKeyVault -VaultName "Contoso03Vault"
```

<span data-ttu-id="f839a-113">Ez a parancs eltávolítja a Contoso03Vault nevű kulcs-boltozatot a jelenlegi előfizetésből.</span><span class="sxs-lookup"><span data-stu-id="f839a-113">This command removes the key vault named Contoso03Vault from your current subscription.</span></span>

### <span data-ttu-id="f839a-114">2. példa: kulcs-boltozat eltávolítása egy megadott erőforráscsoporthoz</span><span class="sxs-lookup"><span data-stu-id="f839a-114">Example 2: Remove a key vault from a specified resource group</span></span>
```
PS C:\>Remove-AzureRmKeyVault -VaultName "Contoso03Vault" -ResourceGroupName "Group14"
```

<span data-ttu-id="f839a-115">Ez a parancs eltávolítja a Contoso03Vault nevű kulcspárt a megnevezett erőforrás csoportból.</span><span class="sxs-lookup"><span data-stu-id="f839a-115">This command removes the key vault named Contoso03Vault from the named resource group.</span></span>
<span data-ttu-id="f839a-116">Ha nem adja meg az erőforráscsoport nevét, a parancsmag a megnevezett kulcs boltozatát keresi a jelenlegi előfizetésben.</span><span class="sxs-lookup"><span data-stu-id="f839a-116">If you do not specify the resource group name, the cmdlet searches for the named key vault to delete in your current subscription.</span></span>

## <span data-ttu-id="f839a-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f839a-117">PARAMETERS</span></span>

### <span data-ttu-id="f839a-118">-Force</span><span class="sxs-lookup"><span data-stu-id="f839a-118">-Force</span></span>
<span data-ttu-id="f839a-119">Azt jelzi, hogy a parancsmag nem kér megerősítést.</span><span class="sxs-lookup"><span data-stu-id="f839a-119">Indicates that the cmdlet does not prompt you for confirmation.</span></span>
<span data-ttu-id="f839a-120">Ez a parancsmag alapértelmezés szerint arra kéri, hogy erősítse meg, hogy törölni szeretné-e a kulcs boltozatát.</span><span class="sxs-lookup"><span data-stu-id="f839a-120">By default, this cmdlet prompts you to confirm that you want to delete the key vault.</span></span>

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

### <span data-ttu-id="f839a-121">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="f839a-121">-InRemovedState</span></span>
<span data-ttu-id="f839a-122">Törölje véglegesen a korábban törölt boltozatot.</span><span class="sxs-lookup"><span data-stu-id="f839a-122">Remove the previously deleted vault permanently.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByDeletedVault
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f839a-123">-Hely</span><span class="sxs-lookup"><span data-stu-id="f839a-123">-Location</span></span>
<span data-ttu-id="f839a-124">A törölt boltozat helye.</span><span class="sxs-lookup"><span data-stu-id="f839a-124">The location of the deleted vault.</span></span>

```yaml
Type: System.String
Parameter Sets: ByAvailableVault
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByDeletedVault
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f839a-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f839a-125">-ResourceGroupName</span></span>
<span data-ttu-id="f839a-126">Egy erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="f839a-126">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ByAvailableVault
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f839a-127">-VaultName</span><span class="sxs-lookup"><span data-stu-id="f839a-127">-VaultName</span></span>
<span data-ttu-id="f839a-128">Az eltávolítandó kulcsfájl nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="f839a-128">Specifies the name of the key vault to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f839a-129">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="f839a-129">-Confirm</span></span>
<span data-ttu-id="f839a-130">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="f839a-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f839a-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f839a-131">-WhatIf</span></span>
<span data-ttu-id="f839a-132">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="f839a-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f839a-133">A parancsmag nem fut. Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="f839a-133">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f839a-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="f839a-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f839a-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f839a-135">-DefaultProfile</span></span>
<span data-ttu-id="f839a-136">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f839a-136">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f839a-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f839a-137">CommonParameters</span></span>
<span data-ttu-id="f839a-138">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f839a-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f839a-139">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f839a-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f839a-140">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f839a-140">INPUTS</span></span>

## <span data-ttu-id="f839a-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f839a-141">OUTPUTS</span></span>

## <span data-ttu-id="f839a-142">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f839a-142">NOTES</span></span>

## <span data-ttu-id="f839a-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f839a-143">RELATED LINKS</span></span>

[<span data-ttu-id="f839a-144">Get-AzureRmKeyVault</span><span class="sxs-lookup"><span data-stu-id="f839a-144">Get-AzureRmKeyVault</span></span>](./Get-AzureRmKeyVault.md)

[<span data-ttu-id="f839a-145">Új – AzureRmKeyVault</span><span class="sxs-lookup"><span data-stu-id="f839a-145">New-AzureRmKeyVault</span></span>](./New-AzureRmKeyVault.md)
