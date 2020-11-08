---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: 4D87DD30-4AEF-4269-93B2-AE5964334AC8
online version: ''
schema: 2.0.0
ms.openlocfilehash: b581712f020b8168c052634e0f20244e16a7d950
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016480"
---
# <span data-ttu-id="03678-101">Remove-AzureAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="03678-101">Remove-AzureAutomationCredential</span></span>

## <span data-ttu-id="03678-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="03678-102">SYNOPSIS</span></span>

<span data-ttu-id="03678-103">Hitelesítő adatok eltávolítása az automatizálásból.</span><span class="sxs-lookup"><span data-stu-id="03678-103">Removes a credential from Automation.</span></span>

## <span data-ttu-id="03678-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="03678-104">SYNTAX</span></span>

```
Remove-AzureAutomationCredential -Name <String> [-Force] -AutomationAccountName <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="03678-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="03678-105">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="03678-106">A **Remove-AzureAutomationCredential** parancsmag eltávolítja a hitelesítő adatokat a Microsoft Azure automatizálási webhelyről.</span><span class="sxs-lookup"><span data-stu-id="03678-106">The **Remove-AzureAutomationCredential** cmdlet removes a credential from Microsoft Azure Automation.</span></span>

## <span data-ttu-id="03678-107">Példák</span><span class="sxs-lookup"><span data-stu-id="03678-107">EXAMPLES</span></span>

### <span data-ttu-id="03678-108">1. példa: hitelesítő adatok eltávolítása</span><span class="sxs-lookup"><span data-stu-id="03678-108">Example 1: Remove a credential</span></span>
```
PS C:\> Remove-AzureAutomationCredential -AutomationAccountName "Contoso17" -Name "MyCredential"
```

<span data-ttu-id="03678-109">Ez a parancs eltávolítja a MyCredential nevű hitelesítő adatokat a Contoso17 nevű automatizálási fiókban.</span><span class="sxs-lookup"><span data-stu-id="03678-109">This command removes a credential named MyCredential in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="03678-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="03678-110">PARAMETERS</span></span>

### <span data-ttu-id="03678-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="03678-111">-AutomationAccountName</span></span>
<span data-ttu-id="03678-112">A hitelesítő adatokkal rendelkező automatizálási fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="03678-112">Specifies the name of the Automation account with the credential.</span></span>

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

### <span data-ttu-id="03678-113">-Force</span><span class="sxs-lookup"><span data-stu-id="03678-113">-Force</span></span>
<span data-ttu-id="03678-114">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="03678-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="03678-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="03678-115">-Name</span></span>
<span data-ttu-id="03678-116">Az eltávolítandó hitelesítő adatok nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="03678-116">Specifies the name of the credential to remove.</span></span>

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

### <span data-ttu-id="03678-117">-Profil</span><span class="sxs-lookup"><span data-stu-id="03678-117">-Profile</span></span>
<span data-ttu-id="03678-118">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="03678-118">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="03678-119">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="03678-119">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="03678-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="03678-120">CommonParameters</span></span>
<span data-ttu-id="03678-121">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="03678-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="03678-122">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="03678-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="03678-123">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="03678-123">INPUTS</span></span>

## <span data-ttu-id="03678-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="03678-124">OUTPUTS</span></span>

## <span data-ttu-id="03678-125">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="03678-125">NOTES</span></span>

## <span data-ttu-id="03678-126">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="03678-126">RELATED LINKS</span></span>

[<span data-ttu-id="03678-127">Get-AzureAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="03678-127">Get-AzureAutomationCredential</span></span>](./Get-AzureAutomationCredential.md)

[<span data-ttu-id="03678-128">Új – AzureAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="03678-128">New-AzureAutomationCredential</span></span>](./New-AzureAutomationCredential.md)

[<span data-ttu-id="03678-129">Set-AzureAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="03678-129">Set-AzureAutomationCredential</span></span>](./Set-AzureAutomationCredential.md)


