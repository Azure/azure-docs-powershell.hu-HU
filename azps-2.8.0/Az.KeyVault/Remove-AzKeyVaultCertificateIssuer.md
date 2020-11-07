---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: FC14F6BF-BD8F-45E0-9CAA-A937E5E56288
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/remove-azkeyvaultcertificateissuer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultCertificateIssuer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultCertificateIssuer.md
ms.openlocfilehash: bca432cb1747ad8333542ec272ef38c2a6c7598f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93666170"
---
# <span data-ttu-id="6fbe6-101">Remove-AzKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="6fbe6-101">Remove-AzKeyVaultCertificateIssuer</span></span>

## <span data-ttu-id="6fbe6-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="6fbe6-102">SYNOPSIS</span></span>
<span data-ttu-id="6fbe6-103">A tanúsítvány kijavítása egy kulcs boltozatról</span><span class="sxs-lookup"><span data-stu-id="6fbe6-103">Deletes a certificate issuer from a key vault.</span></span>

## <span data-ttu-id="6fbe6-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="6fbe6-104">SYNTAX</span></span>

### <span data-ttu-id="6fbe6-105">Alapértelmezett (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="6fbe6-105">Default (Default)</span></span>
```
Remove-AzKeyVaultCertificateIssuer [-VaultName] <String> [-Name] <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6fbe6-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="6fbe6-106">InputObject</span></span>
```
Remove-AzKeyVaultCertificateIssuer [-InputObject] <PSKeyVaultCertificateIssuerIdentityItem> [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6fbe6-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="6fbe6-107">DESCRIPTION</span></span>
<span data-ttu-id="6fbe6-108">A **Remove-AzKeyVaultCertificateIssuer** parancsmag a tanúsítvány kifizetését egy kulcs boltozatról törli.</span><span class="sxs-lookup"><span data-stu-id="6fbe6-108">The **Remove-AzKeyVaultCertificateIssuer** cmdlet deletes a certificate issuer from a key vault.</span></span>

## <span data-ttu-id="6fbe6-109">Példák</span><span class="sxs-lookup"><span data-stu-id="6fbe6-109">EXAMPLES</span></span>

### <span data-ttu-id="6fbe6-110">1. példa: a tanúsítvány kibocsátásának eltávolítása</span><span class="sxs-lookup"><span data-stu-id="6fbe6-110">Example 1: Remove a certificate issuer</span></span>
```powershell
PS C:\> Remove-AzKeyVaultCertificateIssuer -VaultName "ContosoKV01" -Name "TestIssuer01" -Force

AccountId           :
ApiKey              :
OrganizationDetails :
Name                : TestIssuer01
IssuerProvider      : test
VaultName           : ContosoKV01
```

<span data-ttu-id="6fbe6-111">Ez a parancs eltávolítja a TestIssuer01 nevű tanúsítvány-kibocsátási kulcsot a ContosoKV01.</span><span class="sxs-lookup"><span data-stu-id="6fbe6-111">This command removes the certificate issuer named TestIssuer01 from the ContosoKV01 key vault.</span></span>

## <span data-ttu-id="6fbe6-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="6fbe6-112">PARAMETERS</span></span>

### <span data-ttu-id="6fbe6-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6fbe6-113">-DefaultProfile</span></span>
<span data-ttu-id="6fbe6-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="6fbe6-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6fbe6-115">-Force</span><span class="sxs-lookup"><span data-stu-id="6fbe6-115">-Force</span></span>
<span data-ttu-id="6fbe6-116">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="6fbe6-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="6fbe6-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6fbe6-117">-InputObject</span></span>
<span data-ttu-id="6fbe6-118">A tanúsítvány-kibocsátási objektum</span><span class="sxs-lookup"><span data-stu-id="6fbe6-118">Certificate Issuer Object</span></span>

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

### <span data-ttu-id="6fbe6-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="6fbe6-119">-Name</span></span>
<span data-ttu-id="6fbe6-120">Itt adhatja meg az eltávolítandó tanúsítvány nevét.</span><span class="sxs-lookup"><span data-stu-id="6fbe6-120">Specifies the name of the issuer to remove.</span></span>

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

### <span data-ttu-id="6fbe6-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6fbe6-121">-PassThru</span></span>
<span data-ttu-id="6fbe6-122">Egy olyan objektumot ad eredményül, amely a munkaterületet jelképezi.</span><span class="sxs-lookup"><span data-stu-id="6fbe6-122">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="6fbe6-123">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="6fbe6-123">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="6fbe6-124">-VaultName</span><span class="sxs-lookup"><span data-stu-id="6fbe6-124">-VaultName</span></span>
<span data-ttu-id="6fbe6-125">A kulcsfájl nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="6fbe6-125">Specifies the name of a key vault.</span></span>

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

### <span data-ttu-id="6fbe6-126">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="6fbe6-126">-Confirm</span></span>
<span data-ttu-id="6fbe6-127">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="6fbe6-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6fbe6-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6fbe6-128">-WhatIf</span></span>
<span data-ttu-id="6fbe6-129">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="6fbe6-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6fbe6-130">A parancsmag nem fut. Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="6fbe6-130">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6fbe6-131">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="6fbe6-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6fbe6-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6fbe6-132">CommonParameters</span></span>
<span data-ttu-id="6fbe6-133">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="6fbe6-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6fbe6-134">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6fbe6-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6fbe6-135">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="6fbe6-135">INPUTS</span></span>

### <span data-ttu-id="6fbe6-136">Microsoft. Azure. Command. PSKeyVaultCertificateIssuerIdentityItem. models.</span><span class="sxs-lookup"><span data-stu-id="6fbe6-136">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIssuerIdentityItem</span></span>

## <span data-ttu-id="6fbe6-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6fbe6-137">OUTPUTS</span></span>

### <span data-ttu-id="6fbe6-138">Microsoft. Azure. Command. PSKeyVaultCertificateIssuer. models.</span><span class="sxs-lookup"><span data-stu-id="6fbe6-138">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIssuer</span></span>

## <span data-ttu-id="6fbe6-139">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="6fbe6-139">NOTES</span></span>

## <span data-ttu-id="6fbe6-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6fbe6-140">RELATED LINKS</span></span>

[<span data-ttu-id="6fbe6-141">Get-AzKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="6fbe6-141">Get-AzKeyVaultCertificateIssuer</span></span>](./Get-AzKeyVaultCertificateIssuer.md)

[<span data-ttu-id="6fbe6-142">Set-AzKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="6fbe6-142">Set-AzKeyVaultCertificateIssuer</span></span>](./Set-AzKeyVaultCertificateIssuer.md)


