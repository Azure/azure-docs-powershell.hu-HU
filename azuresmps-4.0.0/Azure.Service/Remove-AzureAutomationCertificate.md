---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: BCF8DAB4-3E14-463B-A18F-E91C740B0D3A
online version: ''
schema: 2.0.0
ms.openlocfilehash: 08dd82489bf02efa167386300b9b1d565e1a63de
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016493"
---
# <span data-ttu-id="20f74-101">Remove-AzureAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="20f74-101">Remove-AzureAutomationCertificate</span></span>

## <span data-ttu-id="20f74-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="20f74-102">SYNOPSIS</span></span>

<span data-ttu-id="20f74-103">Automatizálási tanúsítvány eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="20f74-103">Removes an Automation certificate.</span></span>

## <span data-ttu-id="20f74-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="20f74-104">SYNTAX</span></span>

```
Remove-AzureAutomationCertificate -Name <String> [-Force] -AutomationAccountName <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="20f74-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="20f74-105">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="20f74-106">A **Remove-AzureAutomationAccount** parancsmag eltávolítja a tanúsítványt a Microsoft Azure automatizálási webhelyről.</span><span class="sxs-lookup"><span data-stu-id="20f74-106">The **Remove-AzureAutomationAccount** cmdlet removes a certificate from Microsoft Azure Automation.</span></span>

## <span data-ttu-id="20f74-107">Példák</span><span class="sxs-lookup"><span data-stu-id="20f74-107">EXAMPLES</span></span>

### <span data-ttu-id="20f74-108">1. példa: tanúsítvány eltávolítása</span><span class="sxs-lookup"><span data-stu-id="20f74-108">Example 1: Remove a certificate</span></span>
```
PS C:\> Remove-AzureAutomationCertificate -AutomationAccountName "Contoso17" -Name "Cert01"
```

<span data-ttu-id="20f74-109">Ez a parancs eltávolítja a Cert01 nevű tanúsítványt a Contoso17 nevű automatizálási fiókban.</span><span class="sxs-lookup"><span data-stu-id="20f74-109">This command removes a certificate named Cert01 in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="20f74-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="20f74-110">PARAMETERS</span></span>

### <span data-ttu-id="20f74-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="20f74-111">-AutomationAccountName</span></span>
<span data-ttu-id="20f74-112">A tanúsítványt használó automatizálási fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="20f74-112">Specifies the name of the Automation account with the certificate.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="20f74-113">-Force</span><span class="sxs-lookup"><span data-stu-id="20f74-113">-Force</span></span>
<span data-ttu-id="20f74-114">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="20f74-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="20f74-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="20f74-115">-Name</span></span>
<span data-ttu-id="20f74-116">A tanúsítvány nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="20f74-116">Specifies the name of the certificate.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="20f74-117">-Profil</span><span class="sxs-lookup"><span data-stu-id="20f74-117">-Profile</span></span>
<span data-ttu-id="20f74-118">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="20f74-118">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="20f74-119">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="20f74-119">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20f74-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="20f74-120">CommonParameters</span></span>
<span data-ttu-id="20f74-121">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="20f74-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="20f74-122">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="20f74-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="20f74-123">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="20f74-123">INPUTS</span></span>

## <span data-ttu-id="20f74-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="20f74-124">OUTPUTS</span></span>

## <span data-ttu-id="20f74-125">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="20f74-125">NOTES</span></span>

## <span data-ttu-id="20f74-126">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="20f74-126">RELATED LINKS</span></span>

[<span data-ttu-id="20f74-127">Get-AzureAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="20f74-127">Get-AzureAutomationCertificate</span></span>](./Get-AzureAutomationCertificate.md)

[<span data-ttu-id="20f74-128">Új – AzureAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="20f74-128">New-AzureAutomationCertificate</span></span>](./New-AzureAutomationCertificate.md)

[<span data-ttu-id="20f74-129">Set-AzureAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="20f74-129">Set-AzureAutomationCertificate</span></span>](./Set-AzureAutomationCertificate.md)


