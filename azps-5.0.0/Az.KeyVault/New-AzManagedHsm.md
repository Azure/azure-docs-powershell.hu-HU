---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/new-azmanagedhsm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/New-AzManagedHsm.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/New-AzManagedHsm.md
ms.openlocfilehash: 2cab0fedd31f482b2e826a02f686ec8bf651c1bb
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94195920"
---
# <span data-ttu-id="c1bb0-101">New-AzManagedHsm</span><span class="sxs-lookup"><span data-stu-id="c1bb0-101">New-AzManagedHsm</span></span>

## <span data-ttu-id="c1bb0-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c1bb0-102">SYNOPSIS</span></span>
<span data-ttu-id="c1bb0-103">Felügyelt HSM-t hoz létre.</span><span class="sxs-lookup"><span data-stu-id="c1bb0-103">Creates a managed HSM.</span></span>

## <span data-ttu-id="c1bb0-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c1bb0-104">SYNTAX</span></span>

```
New-AzManagedHsm [-Name] <String> [-ResourceGroupName] <String> [-Location] <String>
 [-Administrator] <String[]> [-Sku <String>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c1bb0-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="c1bb0-105">DESCRIPTION</span></span>
<span data-ttu-id="c1bb0-106">A **New-AzManagedHsm** parancsmag létrehoz egy felügyelt HSM-t a megadott erőforráscsoport számára.</span><span class="sxs-lookup"><span data-stu-id="c1bb0-106">The **New-AzManagedHsm** cmdlet creates a managed HSM in the specified resource group.</span></span> <span data-ttu-id="c1bb0-107">Ha a felügyelt HSM alkalmazásban szeretne hozzáadni, eltávolítani vagy listázni a kulcsokat, akkor a felhasználónak felhasználói azonosító hozzáadásával kell engedélyt adni a rendszergazdának.</span><span class="sxs-lookup"><span data-stu-id="c1bb0-107">To add, remove, or list keys in the managed HSM, user should grant permissions by adding user ID to Administrator.</span></span>

## <span data-ttu-id="c1bb0-108">Példák</span><span class="sxs-lookup"><span data-stu-id="c1bb0-108">EXAMPLES</span></span>

### <span data-ttu-id="c1bb0-109">Példa 1: StandardB1 felügyelt HSM létrehozása</span><span class="sxs-lookup"><span data-stu-id="c1bb0-109">Example 1: Create a StandardB1 managed HSM</span></span>
```powershell
PS C:\> New-AzManagedHsm -Name 'myhsm' -ResourceGroupName 'myrg1' -Location 'eastus2euap' -Administrator "xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx"

Name  Resource Group Name Location    SKU
----  ------------------- --------    ---
myhsm myrg1               eastus2euap StandardB1
```

<span data-ttu-id="c1bb0-110">A parancs létrehoz egy myhsm nevű felügyelt HSM-nevet a hely eastus2euap.</span><span class="sxs-lookup"><span data-stu-id="c1bb0-110">This command creates a managed HSM named myhsm in the location eastus2euap.</span></span> <span data-ttu-id="c1bb0-111">A parancs hozzáadja a felügyelt HSM-t a myrg1 nevű erőforráscsoport csoportjához.</span><span class="sxs-lookup"><span data-stu-id="c1bb0-111">The command adds the managed HSM to the resource group named myrg1.</span></span> <span data-ttu-id="c1bb0-112">Mivel a parancs nem ad meg értéket a *SKU* paraméterhez, létrehoz egy Standard_B1 felügyelt HSM-t.</span><span class="sxs-lookup"><span data-stu-id="c1bb0-112">Because the command does not specify a value for the *SKU* parameter, it creates a Standard_B1 managed HSM.</span></span>

### <span data-ttu-id="c1bb0-113">2. példa: CustomB32 felügyelt HSM létrehozása</span><span class="sxs-lookup"><span data-stu-id="c1bb0-113">Example 2: Create a CustomB32 managed HSM</span></span>
```powershell
PS C:\>New-AzManagedHsm -Name 'myhsm' -ResourceGroupName 'myrg1' -Location 'eastus2euap' -Administrator "xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx" -Sku 'CustomB32'
Name  Resource Group Name Location    SKU

----  ------------------- --------    ---
myhsm myrg1               eastus2euap CustomB32
```

                      

<span data-ttu-id="c1bb0-114">Ez a parancs a felügyelt HSM-t az előző példában szereplőhöz hasonlóan hozza létre.</span><span class="sxs-lookup"><span data-stu-id="c1bb0-114">This command creates a managed HSM, just like the previous example.</span></span> <span data-ttu-id="c1bb0-115">A CustomB32 felügyelt HSM létrehozásakor azonban a CustomB32 értékét adja meg a *SKU* paraméterhez.</span><span class="sxs-lookup"><span data-stu-id="c1bb0-115">However, it specifies a value of CustomB32 for the *SKU* parameter to create a CustomB32 managed HSM.</span></span>

## <span data-ttu-id="c1bb0-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c1bb0-116">PARAMETERS</span></span>

### <span data-ttu-id="c1bb0-117">-Administrator</span><span class="sxs-lookup"><span data-stu-id="c1bb0-117">-Administrator</span></span>
<span data-ttu-id="c1bb0-118">A felügyelt HSM-készlet kezdeti rendszergazdai objektumazonosító-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="c1bb0-118">Initial administrator object id for this managed HSM pool.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c1bb0-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c1bb0-119">-AsJob</span></span>
<span data-ttu-id="c1bb0-120">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="c1bb0-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c1bb0-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c1bb0-121">-DefaultProfile</span></span>
<span data-ttu-id="c1bb0-122">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c1bb0-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c1bb0-123">-Hely</span><span class="sxs-lookup"><span data-stu-id="c1bb0-123">-Location</span></span>
<span data-ttu-id="c1bb0-124">Azt az Azure-területet adja meg, amelyben a fő pince hozható létre.</span><span class="sxs-lookup"><span data-stu-id="c1bb0-124">Specifies the Azure region in which to create the key vault.</span></span>
<span data-ttu-id="c1bb0-125">A ProviderNamespace paraméterrel Get-AzResourceProvider paranccsal megtekintheti a kívánt beállításokat.</span><span class="sxs-lookup"><span data-stu-id="c1bb0-125">Use the command Get-AzResourceProvider with the ProviderNamespace parameter to see your choices.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c1bb0-126">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="c1bb0-126">-Name</span></span>
<span data-ttu-id="c1bb0-127">A létrehozandó felügyelt HSM nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="c1bb0-127">Specifies a name of the managed HSM to create.</span></span>
<span data-ttu-id="c1bb0-128">A név lehet betűk, számjegyek és kötőjelek tetszőleges kombinációja.</span><span class="sxs-lookup"><span data-stu-id="c1bb0-128">The name can be any combination of letters, digits, or hyphens.</span></span>
<span data-ttu-id="c1bb0-129">A névnek betűvel vagy számmal kell kezdődnie.</span><span class="sxs-lookup"><span data-stu-id="c1bb0-129">The name must start and end with a letter or digit.</span></span>
<span data-ttu-id="c1bb0-130">A névnek univerzálisan egyedinek kell lennie.</span><span class="sxs-lookup"><span data-stu-id="c1bb0-130">The name must be universally unique.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: HsmName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c1bb0-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c1bb0-131">-ResourceGroupName</span></span>
<span data-ttu-id="c1bb0-132">Annak a meglévő erőforrás-csoportnak a nevét adja meg, amelybe a kulcs boltozatát létre szeretné hozni.</span><span class="sxs-lookup"><span data-stu-id="c1bb0-132">Specifies the name of an existing resource group in which to create the key vault.</span></span>

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

### <span data-ttu-id="c1bb0-133">-SKU</span><span class="sxs-lookup"><span data-stu-id="c1bb0-133">-Sku</span></span>
<span data-ttu-id="c1bb0-134">A felügyelt HSM-példány SKU-ának számát adja meg.</span><span class="sxs-lookup"><span data-stu-id="c1bb0-134">Specifies the SKU of the managed HSM instance.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c1bb0-135">-Címke</span><span class="sxs-lookup"><span data-stu-id="c1bb0-135">-Tag</span></span>
<span data-ttu-id="c1bb0-136">Egy kivonatoló táblázat, amely az erőforrás címkéit jelöli.</span><span class="sxs-lookup"><span data-stu-id="c1bb0-136">A hash table which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c1bb0-137">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="c1bb0-137">-Confirm</span></span>
<span data-ttu-id="c1bb0-138">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="c1bb0-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c1bb0-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c1bb0-139">-WhatIf</span></span>
<span data-ttu-id="c1bb0-140">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="c1bb0-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c1bb0-141">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="c1bb0-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c1bb0-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c1bb0-142">CommonParameters</span></span>
<span data-ttu-id="c1bb0-143">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c1bb0-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c1bb0-144">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="c1bb0-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c1bb0-145">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c1bb0-145">INPUTS</span></span>

### <span data-ttu-id="c1bb0-146">System. String</span><span class="sxs-lookup"><span data-stu-id="c1bb0-146">System.String</span></span>

### <span data-ttu-id="c1bb0-147">System. string []</span><span class="sxs-lookup"><span data-stu-id="c1bb0-147">System.String[]</span></span>

### <span data-ttu-id="c1bb0-148">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="c1bb0-148">System.Collections.Hashtable</span></span>

## <span data-ttu-id="c1bb0-149">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c1bb0-149">OUTPUTS</span></span>

### <span data-ttu-id="c1bb0-150">Microsoft. Azure. Command. PSManagedHsm. models.</span><span class="sxs-lookup"><span data-stu-id="c1bb0-150">Microsoft.Azure.Commands.KeyVault.Models.PSManagedHsm</span></span>

## <span data-ttu-id="c1bb0-151">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c1bb0-151">NOTES</span></span>

## <span data-ttu-id="c1bb0-152">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c1bb0-152">RELATED LINKS</span></span>

[<span data-ttu-id="c1bb0-153">Get-AzManagedHsm</span><span class="sxs-lookup"><span data-stu-id="c1bb0-153">Get-AzManagedHsm</span></span>](./Get-AzManagedHsm.md)

[<span data-ttu-id="c1bb0-154">Remove-AzManagedHsm</span><span class="sxs-lookup"><span data-stu-id="c1bb0-154">Remove-AzManagedHsm</span></span>](./Remove-AzManagedHsm.md)

[<span data-ttu-id="c1bb0-155">Update-AzManagedHsm</span><span class="sxs-lookup"><span data-stu-id="c1bb0-155">Update-AzManagedHsm</span></span>](./Update-AzManagedHsm.md)