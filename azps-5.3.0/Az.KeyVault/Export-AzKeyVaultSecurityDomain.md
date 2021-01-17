---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/export-azkeyvaultsecuritydomain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Export-AzKeyVaultSecurityDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Export-AzKeyVaultSecurityDomain.md
ms.openlocfilehash: 94f27b497450201715b423babbd55811f2382dd2
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98469586"
---
# <span data-ttu-id="db9ac-101">Export-AzKeyVaultSecurityDomain</span><span class="sxs-lookup"><span data-stu-id="db9ac-101">Export-AzKeyVaultSecurityDomain</span></span>

## <span data-ttu-id="db9ac-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="db9ac-102">SYNOPSIS</span></span>
<span data-ttu-id="db9ac-103">Felügyelt HSM biztonsági tartományának adatait exportálja.</span><span class="sxs-lookup"><span data-stu-id="db9ac-103">Exports the security domain data of a managed HSM.</span></span>

## <span data-ttu-id="db9ac-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="db9ac-104">SYNTAX</span></span>

### <span data-ttu-id="db9ac-105">ByName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="db9ac-105">ByName (Default)</span></span>
```
Export-AzKeyVaultSecurityDomain -Certificates <String[]> -OutputPath <String> [-Force] [-PassThru]
 -Quorum <Int32> -Name <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="db9ac-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="db9ac-106">ByInputObject</span></span>
```
Export-AzKeyVaultSecurityDomain -Certificates <String[]> -OutputPath <String> [-Force] [-PassThru]
 -Quorum <Int32> -InputObject <PSKeyVaultIdentityItem> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="db9ac-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="db9ac-107">DESCRIPTION</span></span>
<span data-ttu-id="db9ac-108">Egy felügyelt HSM biztonsági tartományának adatait exportálja egy másik HSM-fájlba való importáláshoz.</span><span class="sxs-lookup"><span data-stu-id="db9ac-108">Exports the security domain data of a managed HSM for importing on another HSM.</span></span>

## <span data-ttu-id="db9ac-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="db9ac-109">EXAMPLES</span></span>

### <span data-ttu-id="db9ac-110">1. példa</span><span class="sxs-lookup"><span data-stu-id="db9ac-110">Example 1</span></span>
```powershell
PS C:\Users\username\> Export-AzKeyVaultSecurityDomain -Name testmhsm -Certificates {pathOfCertificates}/sd1.cer, {pathOfCertificates}/sd2.cer, {pathOfCertificates}/sd3.cer -OutputPath {pathOfOutput}/sd.ps.json -Quorum 2
```

<span data-ttu-id="db9ac-111">Ez a parancs beolvassa a testmhsm nevű felügyelt HSM-et, és a megadott kimeneti fájlba menti a felügyelt HSM biztonsági tartomány biztonsági másolatát.</span><span class="sxs-lookup"><span data-stu-id="db9ac-111">This command retrieves the managed HSM named testmhsm and saves a backup of that managed HSM security domain to the specified output file.</span></span>

## <span data-ttu-id="db9ac-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="db9ac-112">PARAMETERS</span></span>

### <span data-ttu-id="db9ac-113">-Certificates</span><span class="sxs-lookup"><span data-stu-id="db9ac-113">-Certificates</span></span>
<span data-ttu-id="db9ac-114">A biztonsági tartomány adatainak titkosításához használt tanúsítványok elérési útja.</span><span class="sxs-lookup"><span data-stu-id="db9ac-114">Paths to the certificates that are used to encrypt the security domain data.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db9ac-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="db9ac-115">-DefaultProfile</span></span>
<span data-ttu-id="db9ac-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="db9ac-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="db9ac-117">-Force</span><span class="sxs-lookup"><span data-stu-id="db9ac-117">-Force</span></span>
<span data-ttu-id="db9ac-118">Adja meg, hogy felülírja-e a meglévő fájlt.</span><span class="sxs-lookup"><span data-stu-id="db9ac-118">Specify whether to overwrite existing file.</span></span>

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

### <span data-ttu-id="db9ac-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="db9ac-119">-InputObject</span></span>
<span data-ttu-id="db9ac-120">Felügyelt HSM-et képviselő objektum.</span><span class="sxs-lookup"><span data-stu-id="db9ac-120">Object representing a managed HSM.</span></span>

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

### <span data-ttu-id="db9ac-121">-Name</span><span class="sxs-lookup"><span data-stu-id="db9ac-121">-Name</span></span>
<span data-ttu-id="db9ac-122">A felügyelt HSM neve.</span><span class="sxs-lookup"><span data-stu-id="db9ac-122">Name of the managed HSM.</span></span>

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

### <span data-ttu-id="db9ac-123">-OutputPath</span><span class="sxs-lookup"><span data-stu-id="db9ac-123">-OutputPath</span></span>
<span data-ttu-id="db9ac-124">Adja meg, hogy a rendszer hová töltse le a biztonsági tartomány adatait.</span><span class="sxs-lookup"><span data-stu-id="db9ac-124">Specify the path where security domain data will be downloaded to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db9ac-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="db9ac-125">-PassThru</span></span>
<span data-ttu-id="db9ac-126">Ha meg van adva, a parancsmag sikeres visszaadott logikai értéket ad vissza.</span><span class="sxs-lookup"><span data-stu-id="db9ac-126">When specified, a boolean will be returned when cmdlet succeeds.</span></span>

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

### <span data-ttu-id="db9ac-127">– Sivad</span><span class="sxs-lookup"><span data-stu-id="db9ac-127">-Quorum</span></span>
<span data-ttu-id="db9ac-128">A helyreállításhoz a biztonsági tartomány visszafejtéséhez minimálisan szükséges megosztások száma.</span><span class="sxs-lookup"><span data-stu-id="db9ac-128">The minimum number of shares required to decrypt the security domain for recovery.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db9ac-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="db9ac-129">-Confirm</span></span>
<span data-ttu-id="db9ac-130">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="db9ac-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="db9ac-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="db9ac-131">-WhatIf</span></span>
<span data-ttu-id="db9ac-132">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="db9ac-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="db9ac-133">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="db9ac-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="db9ac-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="db9ac-134">CommonParameters</span></span>
<span data-ttu-id="db9ac-135">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="db9ac-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="db9ac-136">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="db9ac-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="db9ac-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="db9ac-137">INPUTS</span></span>

### <span data-ttu-id="db9ac-138">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultIdentityItem</span><span class="sxs-lookup"><span data-stu-id="db9ac-138">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultIdentityItem</span></span>

## <span data-ttu-id="db9ac-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="db9ac-139">OUTPUTS</span></span>

### <span data-ttu-id="db9ac-140">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="db9ac-140">System.Boolean</span></span>

## <span data-ttu-id="db9ac-141">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="db9ac-141">NOTES</span></span>

## <span data-ttu-id="db9ac-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="db9ac-142">RELATED LINKS</span></span>
