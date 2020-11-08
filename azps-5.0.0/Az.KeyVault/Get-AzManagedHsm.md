---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/get-azmanagedhsm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzManagedHsm.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzManagedHsm.md
ms.openlocfilehash: 7a67d6aa0b891c78d644ec7d5f3923a354c3cef1
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94187727"
---
# <span data-ttu-id="c1c86-101">Get-AzManagedHsm</span><span class="sxs-lookup"><span data-stu-id="c1c86-101">Get-AzManagedHsm</span></span>

## <span data-ttu-id="c1c86-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c1c86-102">SYNOPSIS</span></span>
<span data-ttu-id="c1c86-103">Felügyelt HSM beszerzése</span><span class="sxs-lookup"><span data-stu-id="c1c86-103">Get managed HSMs.</span></span>

## <span data-ttu-id="c1c86-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c1c86-104">SYNTAX</span></span>

```
Get-AzManagedHsm [[-Name] <String>] [[-ResourceGroupName] <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c1c86-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="c1c86-105">DESCRIPTION</span></span>
<span data-ttu-id="c1c86-106">A **Get-AzManagedHsm** parancsmag információkat kap az előfizetések felügyelt HSM.</span><span class="sxs-lookup"><span data-stu-id="c1c86-106">The **Get-AzManagedHsm** cmdlet gets information about the managed HSMs in a subscription.</span></span> <span data-ttu-id="c1c86-107">Megtekintheti az előfizetések összes felügyelt HSM példányát, vagy szűrheti a találatokat egy erőforráscsoport vagy egy bizonyos felügyelt HSM segítségével.</span><span class="sxs-lookup"><span data-stu-id="c1c86-107">You can view all managed HSMs instances in a subscription, or filter your results by a resource group or a particular managed HSM.</span></span>
<span data-ttu-id="c1c86-108">Ne feledje, hogy ha egyetlen felügyelt HSM beszerzése esetén az erőforráscsoport nem kötelező, akkor a jobb teljesítmény érdekében ezt a lehetőséget kell tennie.</span><span class="sxs-lookup"><span data-stu-id="c1c86-108">Note that although specifying the resource group is optional for this cmdlet when you get a single managed HSM, you should do so for better performance.</span></span>

## <span data-ttu-id="c1c86-109">Példák</span><span class="sxs-lookup"><span data-stu-id="c1c86-109">EXAMPLES</span></span>

### <span data-ttu-id="c1c86-110">Példa 1: az összes felügyelt HSM beolvasása a jelenlegi előfizetésben</span><span class="sxs-lookup"><span data-stu-id="c1c86-110">Example 1: Get all managed HSMs in your current subscription</span></span>
```powershell
PS C:\> Get-AzManagedHsm

Name  Resource Group Name Location    SKU
----  ------------------- --------    ---
myhsm myrg1               eastus2euap StandardB1
```

<span data-ttu-id="c1c86-111">Ez a parancs beilleszti az összes felügyelt HSM a jelenlegi előfizetésbe.</span><span class="sxs-lookup"><span data-stu-id="c1c86-111">This command gets all managed HSMs in your current subscription.</span></span>

### <span data-ttu-id="c1c86-112">2. példa: meghatározott felügyelt HSM beszerzése</span><span class="sxs-lookup"><span data-stu-id="c1c86-112">Example 2: Get a specific managed HSM</span></span>
```powershell
PS C:\> Get-AzManagedHsm -Name 'myhsm'

Name  Resource Group Name Location    SKU
----  ------------------- --------    ---
myhsm myrg1               eastus2euap StandardB1
```

<span data-ttu-id="c1c86-113">Ez a parancs beolvassa a myhsm nevű felügyelt HSM-t a jelenlegi előfizetésben.</span><span class="sxs-lookup"><span data-stu-id="c1c86-113">This command gets the managed HSM named myhsm in your current subscription.</span></span>

### <span data-ttu-id="c1c86-114">3. példa: felügyelt HSM beszerzése erőforrás-csoportban</span><span class="sxs-lookup"><span data-stu-id="c1c86-114">Example 3: Get managed HSMs in a resource group</span></span>
```powershell
PS C:\> Get-AzManagedHsm -ResourceGroupName 'myrg1'

Name  Resource Group Name Location    SKU
----  ------------------- --------    ---
myhsm myrg1               eastus2euap StandardB1
```

<span data-ttu-id="c1c86-115">Ez a parancs beilleszti az összes felügyelt HSM a myrg1 nevű erőforráscsoport-csoportba.</span><span class="sxs-lookup"><span data-stu-id="c1c86-115">This command gets all managed HSMs in the resource group named myrg1.</span></span>

### <span data-ttu-id="c1c86-116">Példa 4: a felügyelt HSM beszerzése szűréssel</span><span class="sxs-lookup"><span data-stu-id="c1c86-116">Example 4: Get managed HSMs using filtering</span></span>
```powershell
PS C:\> Get-AzManagedHsm -Name 'myhsm*'

Name  Resource Group Name Location    SKU
----  ------------------- --------    ---
myhsm myrg1               eastus2euap StandardB1
```

<span data-ttu-id="c1c86-117">Ez a parancs a "myhsm" kezdetű előfizetés összes felügyelt HSM megkapja.</span><span class="sxs-lookup"><span data-stu-id="c1c86-117">This command gets all managed HSMs in the subscription that start with "myhsm".</span></span>

## <span data-ttu-id="c1c86-118">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c1c86-118">PARAMETERS</span></span>

### <span data-ttu-id="c1c86-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c1c86-119">-DefaultProfile</span></span>
<span data-ttu-id="c1c86-120">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c1c86-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c1c86-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="c1c86-121">-Name</span></span>
<span data-ttu-id="c1c86-122">HSM-név.</span><span class="sxs-lookup"><span data-stu-id="c1c86-122">HSM name.</span></span> <span data-ttu-id="c1c86-123">Parancsmag: a HSM FQDN-t a név és a jelenleg kijelölt környezet alapján építi fel.</span><span class="sxs-lookup"><span data-stu-id="c1c86-123">Cmdlet constructs the FQDN of a HSM based on the name and currently selected environment.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: HsmName

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c1c86-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c1c86-124">-ResourceGroupName</span></span>
<span data-ttu-id="c1c86-125">A felügyelt HSM lekérdezéssel társított erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="c1c86-125">Specifies the name of the resource group associated with the managed HSM being queried.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c1c86-126">-Címke</span><span class="sxs-lookup"><span data-stu-id="c1c86-126">-Tag</span></span>
<span data-ttu-id="c1c86-127">A megadott címke kulcsát és választható értékét adja meg a felügyelt HSM szerinti szűréshez.</span><span class="sxs-lookup"><span data-stu-id="c1c86-127">Specifies the key and optional value of the specified tag to filter the list of managed HSMs by.</span></span>

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

### <span data-ttu-id="c1c86-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c1c86-128">CommonParameters</span></span>
<span data-ttu-id="c1c86-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c1c86-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c1c86-130">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="c1c86-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c1c86-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c1c86-131">INPUTS</span></span>

### <span data-ttu-id="c1c86-132">System. String</span><span class="sxs-lookup"><span data-stu-id="c1c86-132">System.String</span></span>

### <span data-ttu-id="c1c86-133">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="c1c86-133">System.Collections.Hashtable</span></span>

## <span data-ttu-id="c1c86-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c1c86-134">OUTPUTS</span></span>

### <span data-ttu-id="c1c86-135">Microsoft. Azure. Command. PSManagedHsm. models.</span><span class="sxs-lookup"><span data-stu-id="c1c86-135">Microsoft.Azure.Commands.KeyVault.Models.PSManagedHsm</span></span>

### <span data-ttu-id="c1c86-136">Microsoft. Azure. Command. PSKeyVaultIdentityItem. models.</span><span class="sxs-lookup"><span data-stu-id="c1c86-136">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultIdentityItem</span></span>

## <span data-ttu-id="c1c86-137">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c1c86-137">NOTES</span></span>

## <span data-ttu-id="c1c86-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c1c86-138">RELATED LINKS</span></span>

[<span data-ttu-id="c1c86-139">Új – AzManagedHsm</span><span class="sxs-lookup"><span data-stu-id="c1c86-139">New-AzManagedHsm</span></span>](./New-AzManagedHsm.md)

[<span data-ttu-id="c1c86-140">Remove-AzManagedHsm</span><span class="sxs-lookup"><span data-stu-id="c1c86-140">Remove-AzManagedHsm</span></span>](./Remove-AzManagedHsm.md)

[<span data-ttu-id="c1c86-141">Update-AzManagedHsm</span><span class="sxs-lookup"><span data-stu-id="c1c86-141">Update-AzManagedHsm</span></span>](./Update-AzManagedHsm.md)