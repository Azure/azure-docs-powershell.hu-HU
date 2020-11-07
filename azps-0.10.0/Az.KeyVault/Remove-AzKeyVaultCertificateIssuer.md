---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: FC14F6BF-BD8F-45E0-9CAA-A937E5E56288
online version: https://docs.microsoft.com/en-us/powershell/module/Az.keyvault/remove-AzKeyvaultcertificateissuer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Remove-AzKeyVaultCertificateIssuer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Remove-AzKeyVaultCertificateIssuer.md
ms.openlocfilehash: 204ee5a7a4d0e5247ae3de239dce650deb4cff0c
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93842114"
---
# <span data-ttu-id="9dc5f-101">Remove-AzKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="9dc5f-101">Remove-AzKeyVaultCertificateIssuer</span></span>

## <span data-ttu-id="9dc5f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="9dc5f-102">SYNOPSIS</span></span>
<span data-ttu-id="9dc5f-103">A tanúsítvány kijavítása egy kulcs boltozatról</span><span class="sxs-lookup"><span data-stu-id="9dc5f-103">Deletes a certificate issuer from a key vault.</span></span>

## <span data-ttu-id="9dc5f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="9dc5f-104">SYNTAX</span></span>

```
Remove-AzKeyVaultCertificateIssuer [-VaultName] <String> [-Name] <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9dc5f-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="9dc5f-105">DESCRIPTION</span></span>
<span data-ttu-id="9dc5f-106">A **Remove-AzKeyVaultCertificateIssuer** parancsmag a tanúsítvány kifizetését egy kulcs boltozatról törli.</span><span class="sxs-lookup"><span data-stu-id="9dc5f-106">The **Remove-AzKeyVaultCertificateIssuer** cmdlet deletes a certificate issuer from a key vault.</span></span>

## <span data-ttu-id="9dc5f-107">Példák</span><span class="sxs-lookup"><span data-stu-id="9dc5f-107">EXAMPLES</span></span>

### <span data-ttu-id="9dc5f-108">1. példa: a tanúsítvány kibocsátásának eltávolítása</span><span class="sxs-lookup"><span data-stu-id="9dc5f-108">Example 1: Remove a certificate issuer</span></span>
```
PS C:\>Remove-AzKeyVaultCertificateIssuer -VaultName "ContosoKV01" -Name "TestIssuer01" -Force
```

<span data-ttu-id="9dc5f-109">Ez a parancs eltávolítja a TestIssuer01 nevű tanúsítvány-kibocsátási kulcsot a ContosoKV01.</span><span class="sxs-lookup"><span data-stu-id="9dc5f-109">This command removes the certificate issuer named TestIssuer01 from the ContosoKV01 key vault.</span></span>

## <span data-ttu-id="9dc5f-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="9dc5f-110">PARAMETERS</span></span>

### <span data-ttu-id="9dc5f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9dc5f-111">-DefaultProfile</span></span>
<span data-ttu-id="9dc5f-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="9dc5f-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9dc5f-113">-Force</span><span class="sxs-lookup"><span data-stu-id="9dc5f-113">-Force</span></span>
<span data-ttu-id="9dc5f-114">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="9dc5f-114">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9dc5f-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="9dc5f-115">-Name</span></span>
<span data-ttu-id="9dc5f-116">Itt adhatja meg az eltávolítandó tanúsítvány nevét.</span><span class="sxs-lookup"><span data-stu-id="9dc5f-116">Specifies the name of the issuer to remove.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: IssuerName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9dc5f-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9dc5f-117">-PassThru</span></span>
<span data-ttu-id="9dc5f-118">Egy olyan objektumot ad eredményül, amely a munkaterületet jelképezi.</span><span class="sxs-lookup"><span data-stu-id="9dc5f-118">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="9dc5f-119">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="9dc5f-119">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9dc5f-120">-VaultName</span><span class="sxs-lookup"><span data-stu-id="9dc5f-120">-VaultName</span></span>
<span data-ttu-id="9dc5f-121">A kulcsfájl nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="9dc5f-121">Specifies the name of a key vault.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9dc5f-122">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="9dc5f-122">-Confirm</span></span>
<span data-ttu-id="9dc5f-123">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="9dc5f-123">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9dc5f-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9dc5f-124">-WhatIf</span></span>
<span data-ttu-id="9dc5f-125">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="9dc5f-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9dc5f-126">A parancsmag nem fut. Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="9dc5f-126">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9dc5f-127">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="9dc5f-127">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9dc5f-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9dc5f-128">CommonParameters</span></span>
<span data-ttu-id="9dc5f-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="9dc5f-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9dc5f-130">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9dc5f-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9dc5f-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="9dc5f-131">INPUTS</span></span>

### <span data-ttu-id="9dc5f-132">Nincs</span><span class="sxs-lookup"><span data-stu-id="9dc5f-132">None</span></span>
<span data-ttu-id="9dc5f-133">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="9dc5f-133">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="9dc5f-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9dc5f-134">OUTPUTS</span></span>

### <span data-ttu-id="9dc5f-135">Microsoft. Azure. Command. KeyVaultCertificateIssuer. models.</span><span class="sxs-lookup"><span data-stu-id="9dc5f-135">Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificateIssuer</span></span>

## <span data-ttu-id="9dc5f-136">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="9dc5f-136">NOTES</span></span>

## <span data-ttu-id="9dc5f-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9dc5f-137">RELATED LINKS</span></span>

[<span data-ttu-id="9dc5f-138">Get-AzKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="9dc5f-138">Get-AzKeyVaultCertificateIssuer</span></span>](./Get-AzKeyVaultCertificateIssuer.md)

[<span data-ttu-id="9dc5f-139">Set-AzKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="9dc5f-139">Set-AzKeyVaultCertificateIssuer</span></span>](./Set-AzKeyVaultCertificateIssuer.md)


