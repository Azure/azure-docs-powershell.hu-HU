---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/restore-azmanagedhsmsecuritydomain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Restore-AzManagedHsmSecurityDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Restore-AzManagedHsmSecurityDomain.md
ms.openlocfilehash: f743b408917e575005589598a49fafbd8cc95379
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94195905"
---
# <span data-ttu-id="bce6f-101">Restore-AzManagedHsmSecurityDomain</span><span class="sxs-lookup"><span data-stu-id="bce6f-101">Restore-AzManagedHsmSecurityDomain</span></span>

## <span data-ttu-id="bce6f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="bce6f-102">SYNOPSIS</span></span>
<span data-ttu-id="bce6f-103">Az előző biztonsági másolat biztonsági mentése a felügyelt HSM szolgáltatáshoz.</span><span class="sxs-lookup"><span data-stu-id="bce6f-103">Restores previous backed up security domain data to a managed HSM.</span></span>

## <span data-ttu-id="bce6f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="bce6f-104">SYNTAX</span></span>

### <span data-ttu-id="bce6f-105">ByName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="bce6f-105">ByName (Default)</span></span>
```
Restore-AzManagedHsmSecurityDomain -Keys <KeyPath[]> -SecurityDomainPath <String> [-PassThru] -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bce6f-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="bce6f-106">ByInputObject</span></span>
```
Restore-AzManagedHsmSecurityDomain -Keys <KeyPath[]> -SecurityDomainPath <String> [-PassThru]
 -InputObject <PSKeyVaultIdentityItem> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="bce6f-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="bce6f-107">DESCRIPTION</span></span>
<span data-ttu-id="bce6f-108">Ez a parancsmag visszaállítja az előző biztonsági tartomány adatainak biztonsági másolatát a felügyelt HSM-nek.</span><span class="sxs-lookup"><span data-stu-id="bce6f-108">This cmdlet restores previous backed up security domain data to a managed HSM.</span></span>

## <span data-ttu-id="bce6f-109">Példák</span><span class="sxs-lookup"><span data-stu-id="bce6f-109">EXAMPLES</span></span>

### <span data-ttu-id="bce6f-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="bce6f-110">Example 1</span></span>
```powershell
PS C:\> $keys = @{PublicKey = "sd1.cer"; PrivateKey = "sd1.key"}, @{PublicKey = "sd2.cer"; PrivateKey = "sd2.key"}, @{PublicKey = "sd3.cer"; PrivateKey = "sd3.key"}
PS C:\> Restore-AzManagedHsmSecurityDomain -Name testmhsm -Keys $keys -SecurityDomainPath {pathOfBackup}\sd.ps.json
```

<span data-ttu-id="bce6f-111">Először a biztonsági tartomány adatainak visszafejtéséhez szükséges kulcsokat kell megadnia.</span><span class="sxs-lookup"><span data-stu-id="bce6f-111">First, the keys need be provided to decrypt the security domain data.</span></span> <span data-ttu-id="bce6f-112">Ezután a **Restore-AzManagedHsmSecurityDomain** parancs visszaállítja az előző biztonsági tartomány adatainak biztonsági biztonsági másolatát a kezelt HSM-nek a következő billentyűk használatával.</span><span class="sxs-lookup"><span data-stu-id="bce6f-112">Then, The **Restore-AzManagedHsmSecurityDomain** command restores previous backed up security domain data to a managed HSM using these keys.</span></span>

## <span data-ttu-id="bce6f-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="bce6f-113">PARAMETERS</span></span>

### <span data-ttu-id="bce6f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bce6f-114">-DefaultProfile</span></span>
<span data-ttu-id="bce6f-115">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="bce6f-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bce6f-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bce6f-116">-InputObject</span></span>
<span data-ttu-id="bce6f-117">Felügyelt HSM-t képviselő objektum</span><span class="sxs-lookup"><span data-stu-id="bce6f-117">Object representing a managed HSM.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultIdentityItem
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bce6f-118">-Billentyűk</span><span class="sxs-lookup"><span data-stu-id="bce6f-118">-Keys</span></span>
<span data-ttu-id="bce6f-119">A biztonsági tartomány adatainak visszafejtéséhez használt kulcsokra vonatkozó információk.</span><span class="sxs-lookup"><span data-stu-id="bce6f-119">Information about the keys that are used to decrypt the security domain data.</span></span>
<span data-ttu-id="bce6f-120">Ebből a cikkből megtudhatja, hogy miként épül fel a példa.</span><span class="sxs-lookup"><span data-stu-id="bce6f-120">See examples for how it is constructed.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.SecurityDomain.Models.KeyPath[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bce6f-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="bce6f-121">-Name</span></span>
<span data-ttu-id="bce6f-122">A felügyelt HSM neve</span><span class="sxs-lookup"><span data-stu-id="bce6f-122">Name of the managed HSM.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: HsmName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bce6f-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="bce6f-123">-PassThru</span></span>
<span data-ttu-id="bce6f-124">Ha meg van adva egy logikai érték, akkor a parancsmag sikere után egy logikai értéket ad vissza.</span><span class="sxs-lookup"><span data-stu-id="bce6f-124">When specified, a boolean will be returned when cmdlet succeeds.</span></span>

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

### <span data-ttu-id="bce6f-125">-SecurityDomainPath</span><span class="sxs-lookup"><span data-stu-id="bce6f-125">-SecurityDomainPath</span></span>
<span data-ttu-id="bce6f-126">Adja meg a titkosított biztonsági tartomány adatainak elérési útját.</span><span class="sxs-lookup"><span data-stu-id="bce6f-126">Specify the path to the encrypted security domain data.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Path

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bce6f-127">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="bce6f-127">-Confirm</span></span>
<span data-ttu-id="bce6f-128">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="bce6f-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bce6f-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bce6f-129">-WhatIf</span></span>
<span data-ttu-id="bce6f-130">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="bce6f-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bce6f-131">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="bce6f-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bce6f-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bce6f-132">CommonParameters</span></span>
<span data-ttu-id="bce6f-133">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="bce6f-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bce6f-134">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="bce6f-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bce6f-135">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="bce6f-135">INPUTS</span></span>

### <span data-ttu-id="bce6f-136">Microsoft. Azure. Command. PSKeyVaultIdentityItem. models.</span><span class="sxs-lookup"><span data-stu-id="bce6f-136">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultIdentityItem</span></span>

## <span data-ttu-id="bce6f-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="bce6f-137">OUTPUTS</span></span>

### <span data-ttu-id="bce6f-138">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="bce6f-138">System.Boolean</span></span>

## <span data-ttu-id="bce6f-139">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="bce6f-139">NOTES</span></span>

## <span data-ttu-id="bce6f-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="bce6f-140">RELATED LINKS</span></span>
