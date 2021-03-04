---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: FC14F6BF-BD8F-45E0-9CAA-A937E5E56288
online version: https://docs.microsoft.com/powershell/module/az.keyvault/remove-azkeyvaultcertificateissuer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultCertificateIssuer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultCertificateIssuer.md
ms.openlocfilehash: 3a85b92b930ef24e4cb613de28f6a66b530222cf
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101918906"
---
# <span data-ttu-id="5ee09-101">Remove-AzKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="5ee09-101">Remove-AzKeyVaultCertificateIssuer</span></span>

## <span data-ttu-id="5ee09-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5ee09-102">SYNOPSIS</span></span>
<span data-ttu-id="5ee09-103">Törli a tanúsítvány kibocsátóját egy kulcstárolóból.</span><span class="sxs-lookup"><span data-stu-id="5ee09-103">Deletes a certificate issuer from a key vault.</span></span>

## <span data-ttu-id="5ee09-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="5ee09-104">SYNTAX</span></span>

### <span data-ttu-id="5ee09-105">Alapértelmezett (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="5ee09-105">Default (Default)</span></span>
```
Remove-AzKeyVaultCertificateIssuer [-VaultName] <String> [-Name] <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5ee09-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="5ee09-106">InputObject</span></span>
```
Remove-AzKeyVaultCertificateIssuer [-InputObject] <PSKeyVaultCertificateIssuerIdentityItem> [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5ee09-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="5ee09-107">DESCRIPTION</span></span>
<span data-ttu-id="5ee09-108">A **Remove-AzKeyVaultCertificateIssuer** parancsmag törli a tanúsítvány kibocsátóját egy kulcstárolóból.</span><span class="sxs-lookup"><span data-stu-id="5ee09-108">The **Remove-AzKeyVaultCertificateIssuer** cmdlet deletes a certificate issuer from a key vault.</span></span>

## <span data-ttu-id="5ee09-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="5ee09-109">EXAMPLES</span></span>

### <span data-ttu-id="5ee09-110">1. példa: Tanúsítvány kibocsátójának eltávolítása</span><span class="sxs-lookup"><span data-stu-id="5ee09-110">Example 1: Remove a certificate issuer</span></span>
```powershell
PS C:\> Remove-AzKeyVaultCertificateIssuer -VaultName "ContosoKV01" -Name "TestIssuer01" -Force

AccountId           :
ApiKey              :
OrganizationDetails :
Name                : TestIssuer01
IssuerProvider      : test
VaultName           : ContosoKV01
```

<span data-ttu-id="5ee09-111">Ez a parancs eltávolítja a TestIssuer01 nevű tanúsítvány kibocsátóját a ContosoKV01 kulcstárolóból.</span><span class="sxs-lookup"><span data-stu-id="5ee09-111">This command removes the certificate issuer named TestIssuer01 from the ContosoKV01 key vault.</span></span>

## <span data-ttu-id="5ee09-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5ee09-112">PARAMETERS</span></span>

### <span data-ttu-id="5ee09-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5ee09-113">-DefaultProfile</span></span>
<span data-ttu-id="5ee09-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="5ee09-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5ee09-115">-Force</span><span class="sxs-lookup"><span data-stu-id="5ee09-115">-Force</span></span>
<span data-ttu-id="5ee09-116">A parancs futtatását kényszeríti felhasználói megerősítés kérése nélkül.</span><span class="sxs-lookup"><span data-stu-id="5ee09-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="5ee09-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5ee09-117">-InputObject</span></span>
<span data-ttu-id="5ee09-118">Certificate Kibocsátó objektum</span><span class="sxs-lookup"><span data-stu-id="5ee09-118">Certificate Issuer Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIssuerIdentityItem
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5ee09-119">-Name</span><span class="sxs-lookup"><span data-stu-id="5ee09-119">-Name</span></span>
<span data-ttu-id="5ee09-120">Az eltávolítható kibocsátó nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="5ee09-120">Specifies the name of the issuer to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases: IssuerName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ee09-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5ee09-121">-PassThru</span></span>
<span data-ttu-id="5ee09-122">Egy objektumot ad vissza, amely azt az elemet tartalmazza, amellyel dolgozik.</span><span class="sxs-lookup"><span data-stu-id="5ee09-122">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="5ee09-123">Ez a parancsmag alapértelmezés szerint nem hoz létre kimenetet.</span><span class="sxs-lookup"><span data-stu-id="5ee09-123">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="5ee09-124">-VaultName</span><span class="sxs-lookup"><span data-stu-id="5ee09-124">-VaultName</span></span>
<span data-ttu-id="5ee09-125">Egy kulcstár nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="5ee09-125">Specifies the name of a key vault.</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ee09-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5ee09-126">-Confirm</span></span>
<span data-ttu-id="5ee09-127">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="5ee09-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5ee09-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5ee09-128">-WhatIf</span></span>
<span data-ttu-id="5ee09-129">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="5ee09-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5ee09-130">A parancsmag nem fut. A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="5ee09-130">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5ee09-131">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="5ee09-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5ee09-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5ee09-132">CommonParameters</span></span>
<span data-ttu-id="5ee09-133">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5ee09-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5ee09-134">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5ee09-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5ee09-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="5ee09-135">INPUTS</span></span>

### <span data-ttu-id="5ee09-136">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIssuerIdentityItem</span><span class="sxs-lookup"><span data-stu-id="5ee09-136">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIssuerIdentityItem</span></span>

## <span data-ttu-id="5ee09-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5ee09-137">OUTPUTS</span></span>

### <span data-ttu-id="5ee09-138">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="5ee09-138">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIssuer</span></span>

## <span data-ttu-id="5ee09-139">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="5ee09-139">NOTES</span></span>

## <span data-ttu-id="5ee09-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5ee09-140">RELATED LINKS</span></span>

[<span data-ttu-id="5ee09-141">Get-AzKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="5ee09-141">Get-AzKeyVaultCertificateIssuer</span></span>](./Get-AzKeyVaultCertificateIssuer.md)

[<span data-ttu-id="5ee09-142">Set-AzKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="5ee09-142">Set-AzKeyVaultCertificateIssuer</span></span>](./Set-AzKeyVaultCertificateIssuer.md)


