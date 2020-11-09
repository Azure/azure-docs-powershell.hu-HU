---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/backup-azmanagedhsmsecuritydomain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Backup-AzManagedHsmSecurityDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Backup-AzManagedHsmSecurityDomain.md
ms.openlocfilehash: 10a54afa8a6ef2e37beebd9d6cdcd304b2d13979
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94296870"
---
# <span data-ttu-id="2033c-101">Backup-AzManagedHsmSecurityDomain</span><span class="sxs-lookup"><span data-stu-id="2033c-101">Backup-AzManagedHsmSecurityDomain</span></span>

## <span data-ttu-id="2033c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="2033c-102">SYNOPSIS</span></span>
<span data-ttu-id="2033c-103">Biztonsági másolat készítése a felügyelt HSM biztonsági tartományának adatainak visszaállításáról.</span><span class="sxs-lookup"><span data-stu-id="2033c-103">Backs up the security domain data of a managed HSM for restoring.</span></span>

## <span data-ttu-id="2033c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="2033c-104">SYNTAX</span></span>

### <span data-ttu-id="2033c-105">ByName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="2033c-105">ByName (Default)</span></span>
```
Backup-AzManagedHsmSecurityDomain -Certificates <String[]> -OutputPath <String> [-Force] [-PassThru]
 -Quorum <Int32> -Name <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2033c-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="2033c-106">ByInputObject</span></span>
```
Backup-AzManagedHsmSecurityDomain -Certificates <String[]> -OutputPath <String> [-Force] [-PassThru]
 -Quorum <Int32> -InputObject <PSKeyVaultIdentityItem> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2033c-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="2033c-107">DESCRIPTION</span></span>
<span data-ttu-id="2033c-108">Ez a parancsmag biztonsági másolatot hoz létre a felügyelt HSM biztonsági tartományának adatainak visszaállításáról.</span><span class="sxs-lookup"><span data-stu-id="2033c-108">This cmdlet backs up the security domain data of a managed HSM for restoring.</span></span>

## <span data-ttu-id="2033c-109">Példák</span><span class="sxs-lookup"><span data-stu-id="2033c-109">EXAMPLES</span></span>

### <span data-ttu-id="2033c-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="2033c-110">Example 1</span></span>
```powershell
PS C:\Users\username\> Backup-AzManagedHsmSecurityDomain -Name testmhsm -Certificates {pathOfCertificates}/sd1.cer, {pathOfCertificates}/sd2.cer, {pathOfCertificates}/sd3.cer -OutputPath {pathOfOutput}/sd.ps.json -Quorum 2
```

<span data-ttu-id="2033c-111">Ez a parancs beolvassa a testmhsm nevű felügyelt HSM-fájlt, és menti a felügyelt HSM biztonsági tartomány biztonsági másolatát a megadott kimeneti fájlba.</span><span class="sxs-lookup"><span data-stu-id="2033c-111">This command retrieves the managed HSM named testmhsm and saves a backup of that managed HSM security domain to the specified output file.</span></span>

## <span data-ttu-id="2033c-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="2033c-112">PARAMETERS</span></span>

### <span data-ttu-id="2033c-113">-Tanúsítványok</span><span class="sxs-lookup"><span data-stu-id="2033c-113">-Certificates</span></span>
<span data-ttu-id="2033c-114">A biztonsági tartomány adatainak titkosításához használt tanúsítványok elérési útja.</span><span class="sxs-lookup"><span data-stu-id="2033c-114">Paths to the certificates that are used to encrypt the security domain data.</span></span>

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

### <span data-ttu-id="2033c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2033c-115">-DefaultProfile</span></span>
<span data-ttu-id="2033c-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="2033c-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2033c-117">-Force</span><span class="sxs-lookup"><span data-stu-id="2033c-117">-Force</span></span>
<span data-ttu-id="2033c-118">Adja meg, hogy felülírja-e a meglévő fájlt.</span><span class="sxs-lookup"><span data-stu-id="2033c-118">Specify whether to overwrite existing file.</span></span>

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

### <span data-ttu-id="2033c-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2033c-119">-InputObject</span></span>
<span data-ttu-id="2033c-120">Felügyelt HSM-t képviselő objektum</span><span class="sxs-lookup"><span data-stu-id="2033c-120">Object representing a managed HSM.</span></span>

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

### <span data-ttu-id="2033c-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="2033c-121">-Name</span></span>
<span data-ttu-id="2033c-122">A felügyelt HSM neve</span><span class="sxs-lookup"><span data-stu-id="2033c-122">Name of the managed HSM.</span></span>

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

### <span data-ttu-id="2033c-123">-OutputPath</span><span class="sxs-lookup"><span data-stu-id="2033c-123">-OutputPath</span></span>
<span data-ttu-id="2033c-124">Adja meg, hogy milyen elérési utat szeretne letölteni a rendszer a biztonsági tartományba.</span><span class="sxs-lookup"><span data-stu-id="2033c-124">Specify the path where security domain data will be downloaded to.</span></span>

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

### <span data-ttu-id="2033c-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2033c-125">-PassThru</span></span>
<span data-ttu-id="2033c-126">Ha meg van adva egy logikai érték, akkor a parancsmag sikere után egy logikai értéket ad vissza.</span><span class="sxs-lookup"><span data-stu-id="2033c-126">When specified, a boolean will be returned when cmdlet succeeds.</span></span>

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

### <span data-ttu-id="2033c-127">-Kvórum</span><span class="sxs-lookup"><span data-stu-id="2033c-127">-Quorum</span></span>
<span data-ttu-id="2033c-128">A biztonsági tartomány helyreállításhoz való visszafejtéséhez szükséges részvények minimális száma.</span><span class="sxs-lookup"><span data-stu-id="2033c-128">The minimum number of shares required to decrypt the security domain for recovery.</span></span>

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

### <span data-ttu-id="2033c-129">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="2033c-129">-Confirm</span></span>
<span data-ttu-id="2033c-130">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="2033c-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2033c-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2033c-131">-WhatIf</span></span>
<span data-ttu-id="2033c-132">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="2033c-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2033c-133">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="2033c-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2033c-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2033c-134">CommonParameters</span></span>
<span data-ttu-id="2033c-135">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="2033c-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2033c-136">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="2033c-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2033c-137">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="2033c-137">INPUTS</span></span>

### <span data-ttu-id="2033c-138">Microsoft. Azure. Command. PSKeyVaultIdentityItem. models.</span><span class="sxs-lookup"><span data-stu-id="2033c-138">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultIdentityItem</span></span>

## <span data-ttu-id="2033c-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2033c-139">OUTPUTS</span></span>

### <span data-ttu-id="2033c-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="2033c-140">System.Boolean</span></span>

## <span data-ttu-id="2033c-141">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="2033c-141">NOTES</span></span>

## <span data-ttu-id="2033c-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2033c-142">RELATED LINKS</span></span>
