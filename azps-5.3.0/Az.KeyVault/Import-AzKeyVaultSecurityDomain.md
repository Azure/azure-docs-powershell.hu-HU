---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/import-azkeyvaultsecuritydomain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Import-AzKeyVaultSecurityDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Import-AzKeyVaultSecurityDomain.md
ms.openlocfilehash: f96aa323486144ec9d4dcb04ff00f408a763a81a
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98469549"
---
# <span data-ttu-id="dd340-101">Import-AzKeyVaultSecurityDomain</span><span class="sxs-lookup"><span data-stu-id="dd340-101">Import-AzKeyVaultSecurityDomain</span></span>

## <span data-ttu-id="dd340-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dd340-102">SYNOPSIS</span></span>
<span data-ttu-id="dd340-103">A korábban exportált biztonsági tartományadatok importálása felügyelt HSM-fájlba.</span><span class="sxs-lookup"><span data-stu-id="dd340-103">Imports previously exported security domain data to a managed HSM.</span></span>

## <span data-ttu-id="dd340-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="dd340-104">SYNTAX</span></span>

### <span data-ttu-id="dd340-105">ByName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="dd340-105">ByName (Default)</span></span>
```
Import-AzKeyVaultSecurityDomain -Keys <KeyPath[]> -SecurityDomainPath <String> [-PassThru] -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dd340-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="dd340-106">ByInputObject</span></span>
```
Import-AzKeyVaultSecurityDomain -Keys <KeyPath[]> -SecurityDomainPath <String> [-PassThru]
 -InputObject <PSKeyVaultIdentityItem> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="dd340-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="dd340-107">DESCRIPTION</span></span>
<span data-ttu-id="dd340-108">Ez a parancsmag egy felügyelt HSM-fájlba importálja a korábban exportált biztonsági tartományadatokat.</span><span class="sxs-lookup"><span data-stu-id="dd340-108">This cmdlet imports previously exported security domain data to a managed HSM.</span></span>

## <span data-ttu-id="dd340-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="dd340-109">EXAMPLES</span></span>

### <span data-ttu-id="dd340-110">1. példa</span><span class="sxs-lookup"><span data-stu-id="dd340-110">Example 1</span></span>
```powershell
PS C:\> $keys = @{PublicKey = "sd1.cer"; PrivateKey = "sd1.key"}, @{PublicKey = "sd2.cer"; PrivateKey = "sd2.key"}, @{PublicKey = "sd3.cer"; PrivateKey = "sd3.key"}
PS C:\> Import-AzKeyVaultSecurityDomain -Name testmhsm -Keys $keys -SecurityDomainPath {pathOfBackup}\sd.ps.json
```

<span data-ttu-id="dd340-111">Először meg kell adni a kulcsokat a biztonsági tartomány adatainak visszafejtéséhez.</span><span class="sxs-lookup"><span data-stu-id="dd340-111">First, the keys need be provided to decrypt the security domain data.</span></span>
<span data-ttu-id="dd340-112">Ezután az **Import-AzKeyVaultSecurityDomain** parancs visszaállítja az előző biztonsági biztonsági tartományadatokat a felügyelt HSM-be ezekkel a kulcsokkal.</span><span class="sxs-lookup"><span data-stu-id="dd340-112">Then, The **Import-AzKeyVaultSecurityDomain** command restores previous backed up security domain data to a managed HSM using these keys.</span></span>

## <span data-ttu-id="dd340-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="dd340-113">PARAMETERS</span></span>

### <span data-ttu-id="dd340-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dd340-114">-DefaultProfile</span></span>
<span data-ttu-id="dd340-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="dd340-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dd340-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="dd340-116">-InputObject</span></span>
<span data-ttu-id="dd340-117">Felügyelt HSM-et képviselő objektum.</span><span class="sxs-lookup"><span data-stu-id="dd340-117">Object representing a managed HSM.</span></span>

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

### <span data-ttu-id="dd340-118">-Keys</span><span class="sxs-lookup"><span data-stu-id="dd340-118">-Keys</span></span>
<span data-ttu-id="dd340-119">Információk a biztonsági tartomány adatainak visszafejtéséhez használt kulcsokról.</span><span class="sxs-lookup"><span data-stu-id="dd340-119">Information about the keys that are used to decrypt the security domain data.</span></span>
<span data-ttu-id="dd340-120">Tekintsen meg példákat a felépítésére.</span><span class="sxs-lookup"><span data-stu-id="dd340-120">See examples for how it is constructed.</span></span>

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

### <span data-ttu-id="dd340-121">-Name</span><span class="sxs-lookup"><span data-stu-id="dd340-121">-Name</span></span>
<span data-ttu-id="dd340-122">A felügyelt HSM neve.</span><span class="sxs-lookup"><span data-stu-id="dd340-122">Name of the managed HSM.</span></span>

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

### <span data-ttu-id="dd340-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="dd340-123">-PassThru</span></span>
<span data-ttu-id="dd340-124">Ha meg van adva, a parancsmag sikeres visszaadott logikai értéket ad vissza.</span><span class="sxs-lookup"><span data-stu-id="dd340-124">When specified, a boolean will be returned when cmdlet succeeds.</span></span>

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

### <span data-ttu-id="dd340-125">-SecurityDomainPath</span><span class="sxs-lookup"><span data-stu-id="dd340-125">-SecurityDomainPath</span></span>
<span data-ttu-id="dd340-126">Adja meg a titkosított biztonsági tartomány adatainak elérési útját.</span><span class="sxs-lookup"><span data-stu-id="dd340-126">Specify the path to the encrypted security domain data.</span></span>

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

### <span data-ttu-id="dd340-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="dd340-127">-Confirm</span></span>
<span data-ttu-id="dd340-128">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="dd340-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dd340-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dd340-129">-WhatIf</span></span>
<span data-ttu-id="dd340-130">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="dd340-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dd340-131">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="dd340-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dd340-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dd340-132">CommonParameters</span></span>
<span data-ttu-id="dd340-133">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dd340-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dd340-134">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="dd340-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dd340-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="dd340-135">INPUTS</span></span>

### <span data-ttu-id="dd340-136">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultIdentityItem</span><span class="sxs-lookup"><span data-stu-id="dd340-136">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultIdentityItem</span></span>

## <span data-ttu-id="dd340-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="dd340-137">OUTPUTS</span></span>

### <span data-ttu-id="dd340-138">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="dd340-138">System.Boolean</span></span>

## <span data-ttu-id="dd340-139">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="dd340-139">NOTES</span></span>

## <span data-ttu-id="dd340-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="dd340-140">RELATED LINKS</span></span>
