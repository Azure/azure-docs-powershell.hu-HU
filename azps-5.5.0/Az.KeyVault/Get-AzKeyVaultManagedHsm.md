---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/get-azkeyvaultmanagedhsm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultManagedHsm.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultManagedHsm.md
ms.openlocfilehash: 8d602e5cbb3a24307ba77daf9a88a79a3c5bb705
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100147675"
---
# <span data-ttu-id="02eef-101">Get-AzKeyVaultManagedHsm</span><span class="sxs-lookup"><span data-stu-id="02eef-101">Get-AzKeyVaultManagedHsm</span></span>

## <span data-ttu-id="02eef-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="02eef-102">SYNOPSIS</span></span>
<span data-ttu-id="02eef-103">Felügyelt HSM-eket is lekért.</span><span class="sxs-lookup"><span data-stu-id="02eef-103">Get managed HSMs.</span></span>

## <span data-ttu-id="02eef-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="02eef-104">SYNTAX</span></span>

```
Get-AzKeyVaultManagedHsm [[-Name] <String>] [[-ResourceGroupName] <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="02eef-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="02eef-105">DESCRIPTION</span></span>
<span data-ttu-id="02eef-106">A **Get-AzKeyVaultManagedHsm** parancsmag információkat kap az előfizetésben kezelt HSM-ről.</span><span class="sxs-lookup"><span data-stu-id="02eef-106">The **Get-AzKeyVaultManagedHsm** cmdlet gets information about the managed HSMs in a subscription.</span></span> <span data-ttu-id="02eef-107">Az előfizetésben megtekintheti az összes felügyelt HSM-példányt, vagy szűrheti az eredményeket egy erőforráscsoport vagy egy adott felügyelt HSM szerint.</span><span class="sxs-lookup"><span data-stu-id="02eef-107">You can view all managed HSMs instances in a subscription, or filter your results by a resource group or a particular managed HSM.</span></span>
<span data-ttu-id="02eef-108">Vegye figyelembe, hogy bár az erőforráscsoport megadása nem kötelező ebben a parancsmagban, ha egyetlen felügyelt HSM-et kap, a jobb teljesítmény érdekében ezt kell megtennie.</span><span class="sxs-lookup"><span data-stu-id="02eef-108">Note that although specifying the resource group is optional for this cmdlet when you get a single managed HSM, you should do so for better performance.</span></span>

## <span data-ttu-id="02eef-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="02eef-109">EXAMPLES</span></span>

### <span data-ttu-id="02eef-110">1. példa: Az összes felügyelt HSM lekérte az aktuális előfizetésben</span><span class="sxs-lookup"><span data-stu-id="02eef-110">Example 1: Get all managed HSMs in your current subscription</span></span>
```powershell
PS C:\> Get-AzKeyVaultManagedHsm

Name  Resource Group Name Location    SKU
----  ------------------- --------    ---
myhsm myrg1               eastus2euap StandardB1
```

<span data-ttu-id="02eef-111">Ez a parancs az aktuális előfizetés összes felügyelt HSM-ét beveszi.</span><span class="sxs-lookup"><span data-stu-id="02eef-111">This command gets all managed HSMs in your current subscription.</span></span>

### <span data-ttu-id="02eef-112">2. példa: Egy adott felügyelt HSM lekérte</span><span class="sxs-lookup"><span data-stu-id="02eef-112">Example 2: Get a specific managed HSM</span></span>
```powershell
PS C:\> Get-AzKeyVaultManagedHsm -Name 'myhsm'

Name  Resource Group Name Location    SKU
----  ------------------- --------    ---
myhsm myrg1               eastus2euap StandardB1
```

<span data-ttu-id="02eef-113">Ez a parancs a myhsm nevű felügyelt HSM-et kapja meg az aktuális előfizetésében.</span><span class="sxs-lookup"><span data-stu-id="02eef-113">This command gets the managed HSM named myhsm in your current subscription.</span></span>

### <span data-ttu-id="02eef-114">3. példa: Felügyelt HSM-ek lekérte egy erőforráscsoportban</span><span class="sxs-lookup"><span data-stu-id="02eef-114">Example 3: Get managed HSMs in a resource group</span></span>
```powershell
PS C:\> Get-AzKeyVaultManagedHsm -ResourceGroupName 'myrg1'

Name  Resource Group Name Location    SKU
----  ------------------- --------    ---
myhsm myrg1               eastus2euap StandardB1
```

<span data-ttu-id="02eef-115">Ez a parancs a myrg1 nevű erőforráscsoport összes felügyelt HSM-ét beveszi.</span><span class="sxs-lookup"><span data-stu-id="02eef-115">This command gets all managed HSMs in the resource group named myrg1.</span></span>

### <span data-ttu-id="02eef-116">4. példa: Felügyelt HSM-eket szűrhet</span><span class="sxs-lookup"><span data-stu-id="02eef-116">Example 4: Get managed HSMs using filtering</span></span>
```powershell
PS C:\> Get-AzKeyVaultManagedHsm -Name 'myhsm*'

Name  Resource Group Name Location    SKU
----  ------------------- --------    ---
myhsm myrg1               eastus2euap StandardB1
```

<span data-ttu-id="02eef-117">Ez a parancs az előfizetésben a "myhsm" kezdettől indulva megkapja az összes felügyelt HSM-et.</span><span class="sxs-lookup"><span data-stu-id="02eef-117">This command gets all managed HSMs in the subscription that start with "myhsm".</span></span>

## <span data-ttu-id="02eef-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="02eef-118">PARAMETERS</span></span>

### <span data-ttu-id="02eef-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="02eef-119">-DefaultProfile</span></span>
<span data-ttu-id="02eef-120">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="02eef-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="02eef-121">-Name</span><span class="sxs-lookup"><span data-stu-id="02eef-121">-Name</span></span>
<span data-ttu-id="02eef-122">HSM-név.</span><span class="sxs-lookup"><span data-stu-id="02eef-122">HSM name.</span></span> <span data-ttu-id="02eef-123">A parancsmag a HSM teljes tartománynevét a név és a jelenleg kijelölt környezet alapján építi fel.</span><span class="sxs-lookup"><span data-stu-id="02eef-123">Cmdlet constructs the FQDN of a HSM based on the name and currently selected environment.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: HsmName

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="02eef-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="02eef-124">-ResourceGroupName</span></span>
<span data-ttu-id="02eef-125">A lekérdezett felügyelt HSM-hez társított erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="02eef-125">Specifies the name of the resource group associated with the managed HSM being queried.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="02eef-126">-Tag</span><span class="sxs-lookup"><span data-stu-id="02eef-126">-Tag</span></span>
<span data-ttu-id="02eef-127">Megadja a megadott címke kulcsát és opcionális értékét, amely alapján szűrni kell a felügyelt HSM-eket.</span><span class="sxs-lookup"><span data-stu-id="02eef-127">Specifies the key and optional value of the specified tag to filter the list of managed HSMs by.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="02eef-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="02eef-128">CommonParameters</span></span>
<span data-ttu-id="02eef-129">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="02eef-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="02eef-130">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="02eef-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="02eef-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="02eef-131">INPUTS</span></span>

### <span data-ttu-id="02eef-132">System.String</span><span class="sxs-lookup"><span data-stu-id="02eef-132">System.String</span></span>

### <span data-ttu-id="02eef-133">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="02eef-133">System.Collections.Hashtable</span></span>

## <span data-ttu-id="02eef-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="02eef-134">OUTPUTS</span></span>

### <span data-ttu-id="02eef-135">Microsoft.Azure.Commands.KeyVault.Models.PSManagedHsm</span><span class="sxs-lookup"><span data-stu-id="02eef-135">Microsoft.Azure.Commands.KeyVault.Models.PSManagedHsm</span></span>

### <span data-ttu-id="02eef-136">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultIdentityItem</span><span class="sxs-lookup"><span data-stu-id="02eef-136">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultIdentityItem</span></span>

## <span data-ttu-id="02eef-137">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="02eef-137">NOTES</span></span>

## <span data-ttu-id="02eef-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="02eef-138">RELATED LINKS</span></span>

[<span data-ttu-id="02eef-139">New-AzKeyVaultManagedHsm</span><span class="sxs-lookup"><span data-stu-id="02eef-139">New-AzKeyVaultManagedHsm</span></span>](./New-AzKeyVaultManagedHsm.md)

[<span data-ttu-id="02eef-140">Remove-AzKeyVaultManagedHsm</span><span class="sxs-lookup"><span data-stu-id="02eef-140">Remove-AzKeyVaultManagedHsm</span></span>](./Remove-AzKeyVaultManagedHsm.md)

[<span data-ttu-id="02eef-141">Update-AzKeyVaultManagedHsm</span><span class="sxs-lookup"><span data-stu-id="02eef-141">Update-AzKeyVaultManagedHsm</span></span>](./Update-AzKeyVaultManagedHsm.md)