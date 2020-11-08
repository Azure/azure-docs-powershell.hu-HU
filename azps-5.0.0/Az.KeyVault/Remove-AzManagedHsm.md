---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/remove-azmanagedhsm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzManagedHsm.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzManagedHsm.md
ms.openlocfilehash: 6555299726d8dcf443382f72c2aba6324b6b377d
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94185294"
---
# <span data-ttu-id="1936b-101">Remove-AzManagedHsm</span><span class="sxs-lookup"><span data-stu-id="1936b-101">Remove-AzManagedHsm</span></span>

## <span data-ttu-id="1936b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="1936b-102">SYNOPSIS</span></span>
<span data-ttu-id="1936b-103">A felügyelt HSM törlése</span><span class="sxs-lookup"><span data-stu-id="1936b-103">Deletes a managed HSM.</span></span>

## <span data-ttu-id="1936b-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="1936b-104">SYNTAX</span></span>

### <span data-ttu-id="1936b-105">RemoveManagedHsmByName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="1936b-105">RemoveManagedHsmByName (Default)</span></span>
```
Remove-AzManagedHsm [-Name] <String> [[-ResourceGroupName] <String>] [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1936b-106">RemoveManagedHsmByInputObject</span><span class="sxs-lookup"><span data-stu-id="1936b-106">RemoveManagedHsmByInputObject</span></span>
```
Remove-AzManagedHsm [-InputObject] <PSManagedHsm> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1936b-107">RemoveManagedHsmByResourceId</span><span class="sxs-lookup"><span data-stu-id="1936b-107">RemoveManagedHsmByResourceId</span></span>
```
Remove-AzManagedHsm [-ResourceId] <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1936b-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="1936b-108">DESCRIPTION</span></span>
<span data-ttu-id="1936b-109">A **Remove-AzManagedHsm** parancsmag törli a megadott felügyelt HSM-t.</span><span class="sxs-lookup"><span data-stu-id="1936b-109">The **Remove-AzManagedHsm** cmdlet deletes the specified managed HSM.</span></span>
<span data-ttu-id="1936b-110">Az adott példányban található összes kulcsot is törli.</span><span class="sxs-lookup"><span data-stu-id="1936b-110">It also deletes all keys contained in that instance.</span></span>
<span data-ttu-id="1936b-111">Fontos tudni, hogy az erőforráscsoport megadása esetén a parancsmag nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="1936b-111">Note that although specifying the resource group is optional for this cmdlet, you should so for better performance.</span></span>

## <span data-ttu-id="1936b-112">Példák</span><span class="sxs-lookup"><span data-stu-id="1936b-112">EXAMPLES</span></span>

### <span data-ttu-id="1936b-113">1. példa: felügyelt HSM eltávolítása</span><span class="sxs-lookup"><span data-stu-id="1936b-113">Example 1: Remove a managed HSM</span></span>
```powershell
PS C:\> Remove-AzManagedHsm -HsmName 'myhsm' -Force

True
```

<span data-ttu-id="1936b-114">Ez a parancs eltávolítja a myhsm nevű felügyelt HSM-t a jelenlegi előfizetésből.</span><span class="sxs-lookup"><span data-stu-id="1936b-114">This command removes the managed hsm named myhsm from your current subscription.</span></span>

### <span data-ttu-id="1936b-115">2. példa: a felügyelt HSM eltávolítása egy megadott erőforráscsoport-csoportból</span><span class="sxs-lookup"><span data-stu-id="1936b-115">Example 2: Remove a managed hsm from a specified resource group</span></span>
```powershell
PS C:\> Remove-AzManagedHsm -HsmName 'myhsm' -ResourceGroupName "myrg1" -PassThru

True
```

<span data-ttu-id="1936b-116">Ez a parancs eltávolítja a myhsm nevű felügyelt HSM nevet a myrg1 nevű erőforráscsoport nevében.</span><span class="sxs-lookup"><span data-stu-id="1936b-116">This command removes the managed hsm named myhsm from the resource group named myrg1.</span></span>
<span data-ttu-id="1936b-117">Ha nem adja meg az erőforráscsoport nevét, a parancsmag a megnevezett felügyelt HSM-t keresi a jelenlegi előfizetésben való törléshez.</span><span class="sxs-lookup"><span data-stu-id="1936b-117">If you do not specify the resource group name, the cmdlet searches for the named managed HSM to delete in your current subscription.</span></span>

## <span data-ttu-id="1936b-118">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="1936b-118">PARAMETERS</span></span>

### <span data-ttu-id="1936b-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1936b-119">-AsJob</span></span>
<span data-ttu-id="1936b-120">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="1936b-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1936b-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1936b-121">-DefaultProfile</span></span>
<span data-ttu-id="1936b-122">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="1936b-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1936b-123">-Force</span><span class="sxs-lookup"><span data-stu-id="1936b-123">-Force</span></span>
<span data-ttu-id="1936b-124">Azt jelzi, hogy a parancsmag nem kér megerősítést.</span><span class="sxs-lookup"><span data-stu-id="1936b-124">Indicates that the cmdlet does not prompt you for confirmation.</span></span>
<span data-ttu-id="1936b-125">Ez a parancsmag alapértelmezés szerint arra kéri, hogy erősítse meg, hogy törölni szeretné-e a felügyelt HSM-t.</span><span class="sxs-lookup"><span data-stu-id="1936b-125">By default, this cmdlet prompts you to confirm that you want to delete the managed HSM.</span></span>

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

### <span data-ttu-id="1936b-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1936b-126">-InputObject</span></span>
<span data-ttu-id="1936b-127">A felügyelt HSM-objektumot törölni kell.</span><span class="sxs-lookup"><span data-stu-id="1936b-127">Managed HSM object to be deleted.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSManagedHsm
Parameter Sets: RemoveManagedHsmByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1936b-128">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="1936b-128">-Name</span></span>
<span data-ttu-id="1936b-129">Az eltávolítandó felügyelt HSM nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="1936b-129">Specifies the name of the managed HSM to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveManagedHsmByName
Aliases: HsmName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1936b-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1936b-130">-PassThru</span></span>
<span data-ttu-id="1936b-131">Ez a parancsmag alapértelmezés szerint nem ad vissza objektumot.</span><span class="sxs-lookup"><span data-stu-id="1936b-131">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="1936b-132">Ha meg van adva ez a kapcsoló, az eredmény igaz, ha sikeres.</span><span class="sxs-lookup"><span data-stu-id="1936b-132">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="1936b-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1936b-133">-ResourceGroupName</span></span>
<span data-ttu-id="1936b-134">Az Azure felügyelt HSM erőforrás csoportjának nevét adja meg az eltávolításhoz.</span><span class="sxs-lookup"><span data-stu-id="1936b-134">Specifies the name of resource group for Azure managed HSM to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveManagedHsmByName
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1936b-135">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1936b-135">-ResourceId</span></span>
<span data-ttu-id="1936b-136">ManagedHsm erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="1936b-136">ManagedHsm Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveManagedHsmByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1936b-137">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="1936b-137">-Confirm</span></span>
<span data-ttu-id="1936b-138">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="1936b-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1936b-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1936b-139">-WhatIf</span></span>
<span data-ttu-id="1936b-140">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="1936b-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1936b-141">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="1936b-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1936b-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1936b-142">CommonParameters</span></span>
<span data-ttu-id="1936b-143">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="1936b-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1936b-144">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="1936b-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1936b-145">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="1936b-145">INPUTS</span></span>

### <span data-ttu-id="1936b-146">Microsoft. Azure. Command. PSManagedHsm. models.</span><span class="sxs-lookup"><span data-stu-id="1936b-146">Microsoft.Azure.Commands.KeyVault.Models.PSManagedHsm</span></span>

### <span data-ttu-id="1936b-147">System. String</span><span class="sxs-lookup"><span data-stu-id="1936b-147">System.String</span></span>

## <span data-ttu-id="1936b-148">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1936b-148">OUTPUTS</span></span>

### <span data-ttu-id="1936b-149">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="1936b-149">System.Boolean</span></span>

## <span data-ttu-id="1936b-150">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="1936b-150">NOTES</span></span>

## <span data-ttu-id="1936b-151">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1936b-151">RELATED LINKS</span></span>

[<span data-ttu-id="1936b-152">Get-AzManagedHsm</span><span class="sxs-lookup"><span data-stu-id="1936b-152">Get-AzManagedHsm</span></span>](./Get-AzManagedHsm.md)

[<span data-ttu-id="1936b-153">Új – AzManagedHsm</span><span class="sxs-lookup"><span data-stu-id="1936b-153">New-AzManagedHsm</span></span>](./New-AzManagedHsm.md)

[<span data-ttu-id="1936b-154">Update-AzManagedHsm</span><span class="sxs-lookup"><span data-stu-id="1936b-154">Update-AzManagedHsm</span></span>](./Update-AzManagedHsm.md)