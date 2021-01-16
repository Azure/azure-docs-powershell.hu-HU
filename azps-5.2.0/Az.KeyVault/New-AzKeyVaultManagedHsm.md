---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/new-azkeyvaultmanagedhsm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/New-AzKeyVaultManagedHsm.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/New-AzKeyVaultManagedHsm.md
ms.openlocfilehash: 7d3cd39a18f7cbbd9663d656921375daa490b32e
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98337014"
---
# <span data-ttu-id="26118-101">New-AzKeyVaultManagedHsm</span><span class="sxs-lookup"><span data-stu-id="26118-101">New-AzKeyVaultManagedHsm</span></span>

## <span data-ttu-id="26118-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="26118-102">SYNOPSIS</span></span>
<span data-ttu-id="26118-103">Felügyelt HSM-et hoz létre.</span><span class="sxs-lookup"><span data-stu-id="26118-103">Creates a managed HSM.</span></span>

## <span data-ttu-id="26118-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="26118-104">SYNTAX</span></span>

```
New-AzKeyVaultManagedHsm [-Name] <String> [-ResourceGroupName] <String> [-Location] <String>
 [-Administrator] <String[]> [-Sku <String>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="26118-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="26118-105">DESCRIPTION</span></span>
<span data-ttu-id="26118-106">A **New-AzKeyVaultManagedHsm** parancsmag felügyelt HSM-et hoz létre a megadott erőforráscsoportban.</span><span class="sxs-lookup"><span data-stu-id="26118-106">The **New-AzKeyVaultManagedHsm** cmdlet creates a managed HSM in the specified resource group.</span></span> <span data-ttu-id="26118-107">Ha kulcsokat szeretne hozzáadni, eltávolítani vagy listakulcsokat hozzáadni a felügyelt HSM-hez, a felhasználónak felhasználói azonosítót kell hozzáadnia a rendszergazdához.</span><span class="sxs-lookup"><span data-stu-id="26118-107">To add, remove, or list keys in the managed HSM, user should grant permissions by adding user ID to Administrator.</span></span>

## <span data-ttu-id="26118-108">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="26118-108">EXAMPLES</span></span>

### <span data-ttu-id="26118-109">1. példa: StandardB1 felügyelt HSM létrehozása</span><span class="sxs-lookup"><span data-stu-id="26118-109">Example 1: Create a StandardB1 managed HSM</span></span>
```powershell
PS C:\> New-AzKeyVaultManagedHsm -Name 'myhsm' -ResourceGroupName 'myrg1' -Location 'eastus2euap' -Administrator "xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx"

Name  Resource Group Name Location    SKU
----  ------------------- --------    ---
myhsm myrg1               eastus2euap StandardB1
```

<span data-ttu-id="26118-110">Ez a parancs létrehoz egy myhsm nevű felügyelt HSM-et az eastus2apap helyen.</span><span class="sxs-lookup"><span data-stu-id="26118-110">This command creates a managed HSM named myhsm in the location eastus2euap.</span></span> <span data-ttu-id="26118-111">A parancs hozzáadja a felügyelt HSM-et a myrg1 nevű erőforráscsoporthoz.</span><span class="sxs-lookup"><span data-stu-id="26118-111">The command adds the managed HSM to the resource group named myrg1.</span></span> <span data-ttu-id="26118-112">Mivel a parancs nem ad meg értéket az *SKU* paraméterhez, egy felügyelt HSM Standard_B1 hoz létre.</span><span class="sxs-lookup"><span data-stu-id="26118-112">Because the command does not specify a value for the *SKU* parameter, it creates a Standard_B1 managed HSM.</span></span>

### <span data-ttu-id="26118-113">2. példa: EgyéniB32 felügyelt HSM létrehozása</span><span class="sxs-lookup"><span data-stu-id="26118-113">Example 2: Create a CustomB32 managed HSM</span></span>
```powershell
PS C:\>New-AzKeyVaultManagedHsm -Name 'myhsm' -ResourceGroupName 'myrg1' -Location 'eastus2euap' -Administrator "xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx" -Sku 'CustomB32'
Name  Resource Group Name Location    SKU

----  ------------------- --------    ---
myhsm myrg1               eastus2euap CustomB32
```

                      

<span data-ttu-id="26118-114">Ez a parancs a korábbi példához hasonló felügyelt HSM-et hoz létre.</span><span class="sxs-lookup"><span data-stu-id="26118-114">This command creates a managed HSM, just like the previous example.</span></span> <span data-ttu-id="26118-115">Az EgyéniB32 felügyelt HSM létrehozásához azonban megad egy CustomB32 értéket az *SKU* paraméterhez.</span><span class="sxs-lookup"><span data-stu-id="26118-115">However, it specifies a value of CustomB32 for the *SKU* parameter to create a CustomB32 managed HSM.</span></span>

## <span data-ttu-id="26118-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="26118-116">PARAMETERS</span></span>

### <span data-ttu-id="26118-117">- Rendszergazda</span><span class="sxs-lookup"><span data-stu-id="26118-117">-Administrator</span></span>
<span data-ttu-id="26118-118">A felügyelt HSM-készlet kezdeti rendszergazdai objektumazonosítója.</span><span class="sxs-lookup"><span data-stu-id="26118-118">Initial administrator object id for this managed HSM pool.</span></span>

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

### <span data-ttu-id="26118-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="26118-119">-AsJob</span></span>
<span data-ttu-id="26118-120">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="26118-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="26118-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="26118-121">-DefaultProfile</span></span>
<span data-ttu-id="26118-122">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="26118-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="26118-123">-Location</span><span class="sxs-lookup"><span data-stu-id="26118-123">-Location</span></span>
<span data-ttu-id="26118-124">Megadja azt az Azure-régiót, amelyben létre kell hoznia a kulcstárat.</span><span class="sxs-lookup"><span data-stu-id="26118-124">Specifies the Azure region in which to create the key vault.</span></span>
<span data-ttu-id="26118-125">A választható lehetőségek Get-AzResourceProvider a ProviderNamespace paraméterrel megadott parancsokkal.</span><span class="sxs-lookup"><span data-stu-id="26118-125">Use the command Get-AzResourceProvider with the ProviderNamespace parameter to see your choices.</span></span>

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

### <span data-ttu-id="26118-126">-Name</span><span class="sxs-lookup"><span data-stu-id="26118-126">-Name</span></span>
<span data-ttu-id="26118-127">Megadja a létrehozni szükséges felügyelt HSM nevét.</span><span class="sxs-lookup"><span data-stu-id="26118-127">Specifies a name of the managed HSM to create.</span></span>
<span data-ttu-id="26118-128">A név betűk, számjegyek vagy kötőjelek bármilyen kombinációja lehet.</span><span class="sxs-lookup"><span data-stu-id="26118-128">The name can be any combination of letters, digits, or hyphens.</span></span>
<span data-ttu-id="26118-129">A névnek betűvel vagy számjegysel kell kezdődnie és végződnie.</span><span class="sxs-lookup"><span data-stu-id="26118-129">The name must start and end with a letter or digit.</span></span>
<span data-ttu-id="26118-130">A névnek univerzálisan egyedinek kell lennie.</span><span class="sxs-lookup"><span data-stu-id="26118-130">The name must be universally unique.</span></span>

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

### <span data-ttu-id="26118-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="26118-131">-ResourceGroupName</span></span>
<span data-ttu-id="26118-132">Egy meglévő erőforráscsoport nevét adja meg, amelyben létre kell hoznia a kulcstárat.</span><span class="sxs-lookup"><span data-stu-id="26118-132">Specifies the name of an existing resource group in which to create the key vault.</span></span>

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

### <span data-ttu-id="26118-133">-Termékváltozat</span><span class="sxs-lookup"><span data-stu-id="26118-133">-Sku</span></span>
<span data-ttu-id="26118-134">A felügyelt HSM-példány termékváltozatát adja meg.</span><span class="sxs-lookup"><span data-stu-id="26118-134">Specifies the SKU of the managed HSM instance.</span></span>

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

### <span data-ttu-id="26118-135">-Tag</span><span class="sxs-lookup"><span data-stu-id="26118-135">-Tag</span></span>
<span data-ttu-id="26118-136">A hash table which represents resource tags.</span><span class="sxs-lookup"><span data-stu-id="26118-136">A hash table which represents resource tags.</span></span>

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

### <span data-ttu-id="26118-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="26118-137">-Confirm</span></span>
<span data-ttu-id="26118-138">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="26118-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="26118-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="26118-139">-WhatIf</span></span>
<span data-ttu-id="26118-140">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="26118-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="26118-141">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="26118-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="26118-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="26118-142">CommonParameters</span></span>
<span data-ttu-id="26118-143">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="26118-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="26118-144">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="26118-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="26118-145">INPUTS</span><span class="sxs-lookup"><span data-stu-id="26118-145">INPUTS</span></span>

### <span data-ttu-id="26118-146">System.String</span><span class="sxs-lookup"><span data-stu-id="26118-146">System.String</span></span>

### <span data-ttu-id="26118-147">System.String[]</span><span class="sxs-lookup"><span data-stu-id="26118-147">System.String[]</span></span>

### <span data-ttu-id="26118-148">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="26118-148">System.Collections.Hashtable</span></span>

## <span data-ttu-id="26118-149">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="26118-149">OUTPUTS</span></span>

### <span data-ttu-id="26118-150">Microsoft.Azure.Commands.KeyVault.Models.PSManagedHsm</span><span class="sxs-lookup"><span data-stu-id="26118-150">Microsoft.Azure.Commands.KeyVault.Models.PSManagedHsm</span></span>

## <span data-ttu-id="26118-151">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="26118-151">NOTES</span></span>

## <span data-ttu-id="26118-152">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="26118-152">RELATED LINKS</span></span>

[<span data-ttu-id="26118-153">Get-AzKeyVaultManagedHsm</span><span class="sxs-lookup"><span data-stu-id="26118-153">Get-AzKeyVaultManagedHsm</span></span>](./Get-AzKeyVaultManagedHsm.md)

[<span data-ttu-id="26118-154">Remove-AzKeyVaultManagedHsm</span><span class="sxs-lookup"><span data-stu-id="26118-154">Remove-AzKeyVaultManagedHsm</span></span>](./Remove-AzKeyVaultManagedHsm.md)

[<span data-ttu-id="26118-155">Update-AzKeyVaultManagedHsm</span><span class="sxs-lookup"><span data-stu-id="26118-155">Update-AzKeyVaultManagedHsm</span></span>](./Update-AzKeyVaultManagedHsm.md)