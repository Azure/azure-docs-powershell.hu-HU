---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: FC14F6BF-BD8F-45E0-9CAA-A937E5E56288
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/remove-azurekeyvaultcertificateissuer
schema: 2.0.0
ms.openlocfilehash: 4c732cdfc175c47e9bd8125234cb1d33f1b19097
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93848225"
---
# <span data-ttu-id="de424-101">Remove-AzureKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="de424-101">Remove-AzureKeyVaultCertificateIssuer</span></span>

## <span data-ttu-id="de424-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="de424-102">SYNOPSIS</span></span>
<span data-ttu-id="de424-103">A tanúsítvány kijavítása egy kulcs boltozatról</span><span class="sxs-lookup"><span data-stu-id="de424-103">Deletes a certificate issuer from a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="de424-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="de424-104">SYNTAX</span></span>

```
Remove-AzureKeyVaultCertificateIssuer [-VaultName] <String> [-Name] <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="de424-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="de424-105">DESCRIPTION</span></span>
<span data-ttu-id="de424-106">A **Remove-AzureKeyVaultCertificateIssuer** parancsmag a tanúsítvány kifizetését egy kulcs boltozatról törli.</span><span class="sxs-lookup"><span data-stu-id="de424-106">The **Remove-AzureKeyVaultCertificateIssuer** cmdlet deletes a certificate issuer from a key vault.</span></span>

## <span data-ttu-id="de424-107">Példák</span><span class="sxs-lookup"><span data-stu-id="de424-107">EXAMPLES</span></span>

### <span data-ttu-id="de424-108">1. példa: a tanúsítvány kibocsátásának eltávolítása</span><span class="sxs-lookup"><span data-stu-id="de424-108">Example 1: Remove a certificate issuer</span></span>
```
PS C:\>Remove-AzureKeyVaultCertificateIssuer -VaultName "ContosoKV01" -Name "TestIssuer01" -Force
```

<span data-ttu-id="de424-109">Ez a parancs eltávolítja a TestIssuer01 nevű tanúsítvány-kibocsátási kulcsot a ContosoKV01.</span><span class="sxs-lookup"><span data-stu-id="de424-109">This command removes the certificate issuer named TestIssuer01 from the ContosoKV01 key vault.</span></span>

## <span data-ttu-id="de424-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="de424-110">PARAMETERS</span></span>

### <span data-ttu-id="de424-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="de424-111">-DefaultProfile</span></span>
<span data-ttu-id="de424-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="de424-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="de424-113">-Force</span><span class="sxs-lookup"><span data-stu-id="de424-113">-Force</span></span>
<span data-ttu-id="de424-114">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="de424-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="de424-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="de424-115">-Name</span></span>
<span data-ttu-id="de424-116">Itt adhatja meg az eltávolítandó tanúsítvány nevét.</span><span class="sxs-lookup"><span data-stu-id="de424-116">Specifies the name of the issuer to remove.</span></span>

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

### <span data-ttu-id="de424-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="de424-117">-PassThru</span></span>
<span data-ttu-id="de424-118">Egy olyan objektumot ad eredményül, amely a munkaterületet jelképezi.</span><span class="sxs-lookup"><span data-stu-id="de424-118">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="de424-119">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="de424-119">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="de424-120">-VaultName</span><span class="sxs-lookup"><span data-stu-id="de424-120">-VaultName</span></span>
<span data-ttu-id="de424-121">A kulcsfájl nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="de424-121">Specifies the name of a key vault.</span></span>

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

### <span data-ttu-id="de424-122">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="de424-122">-Confirm</span></span>
<span data-ttu-id="de424-123">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="de424-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="de424-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="de424-124">-WhatIf</span></span>
<span data-ttu-id="de424-125">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="de424-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="de424-126">A parancsmag nem fut. Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="de424-126">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="de424-127">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="de424-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="de424-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="de424-128">CommonParameters</span></span>
<span data-ttu-id="de424-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="de424-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="de424-130">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="de424-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="de424-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="de424-131">INPUTS</span></span>

## <span data-ttu-id="de424-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="de424-132">OUTPUTS</span></span>

### <span data-ttu-id="de424-133">Microsoft. Azure. Command. KeyVaultCertificateIssuer. models.</span><span class="sxs-lookup"><span data-stu-id="de424-133">Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificateIssuer</span></span>

## <span data-ttu-id="de424-134">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="de424-134">NOTES</span></span>

## <span data-ttu-id="de424-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="de424-135">RELATED LINKS</span></span>

[<span data-ttu-id="de424-136">Get-AzureKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="de424-136">Get-AzureKeyVaultCertificateIssuer</span></span>](./Get-AzureKeyVaultCertificateIssuer.md)

[<span data-ttu-id="de424-137">Set-AzureKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="de424-137">Set-AzureKeyVaultCertificateIssuer</span></span>](./Set-AzureKeyVaultCertificateIssuer.md)


