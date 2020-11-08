---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: DDEBA3E1-B5A3-4F16-9A67-A95D15851A33
online version: ''
schema: 2.0.0
ms.openlocfilehash: 0899349c3dbfa368b3ce0dbb4d4085c3ea527c43
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016492"
---
# <span data-ttu-id="2e298-101">Remove-AzureAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="2e298-101">Remove-AzureAutomationConnection</span></span>

## <span data-ttu-id="2e298-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="2e298-102">SYNOPSIS</span></span>

<span data-ttu-id="2e298-103">A kapcsolat eltávolítása az automatizálásból.</span><span class="sxs-lookup"><span data-stu-id="2e298-103">Removes a connection from Automation.</span></span>

## <span data-ttu-id="2e298-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="2e298-104">SYNTAX</span></span>

```
Remove-AzureAutomationConnection -Name <String> [-Force] -AutomationAccountName <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="2e298-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="2e298-105">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="2e298-106">A **Remove-AzureAutomationConnection** parancsmag eltávolítja a kapcsolatot a Microsoft Azure automatizálási webhelyről.</span><span class="sxs-lookup"><span data-stu-id="2e298-106">The **Remove-AzureAutomationConnection** cmdlet removes a connection from Microsoft Azure Automation.</span></span>

## <span data-ttu-id="2e298-107">Példák</span><span class="sxs-lookup"><span data-stu-id="2e298-107">EXAMPLES</span></span>

### <span data-ttu-id="2e298-108">1. példa: kapcsolat eltávolítása</span><span class="sxs-lookup"><span data-stu-id="2e298-108">Example 1: Remove a connection</span></span>
```
PS C:\> Remove-AzureAutomationConnection -AutomationAccountName "Contoso17" -Name "MyConnection"
```

<span data-ttu-id="2e298-109">Ez a parancs eltávolítja a kapcsolatom nevű tanúsítványt a Contoso17 nevű automatizálási fiókban.</span><span class="sxs-lookup"><span data-stu-id="2e298-109">This command removes a certificate named MyConnection in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="2e298-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="2e298-110">PARAMETERS</span></span>

### <span data-ttu-id="2e298-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="2e298-111">-AutomationAccountName</span></span>
<span data-ttu-id="2e298-112">A hitelesítő adatokkal rendelkező automatizálási fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="2e298-112">Specifies the name of the Automation account with the credential.</span></span>

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

### <span data-ttu-id="2e298-113">-Force</span><span class="sxs-lookup"><span data-stu-id="2e298-113">-Force</span></span>
<span data-ttu-id="2e298-114">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="2e298-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="2e298-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="2e298-115">-Name</span></span>
<span data-ttu-id="2e298-116">A kapcsolat nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="2e298-116">Specifies the name of the connection.</span></span>

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

### <span data-ttu-id="2e298-117">-Profil</span><span class="sxs-lookup"><span data-stu-id="2e298-117">-Profile</span></span>
<span data-ttu-id="2e298-118">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="2e298-118">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="2e298-119">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="2e298-119">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="2e298-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2e298-120">CommonParameters</span></span>
<span data-ttu-id="2e298-121">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="2e298-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2e298-122">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2e298-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2e298-123">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="2e298-123">INPUTS</span></span>

## <span data-ttu-id="2e298-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2e298-124">OUTPUTS</span></span>

## <span data-ttu-id="2e298-125">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="2e298-125">NOTES</span></span>

## <span data-ttu-id="2e298-126">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2e298-126">RELATED LINKS</span></span>

[<span data-ttu-id="2e298-127">Get-AzureAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="2e298-127">Get-AzureAutomationConnection</span></span>](./Get-AzureAutomationConnection.md)

[<span data-ttu-id="2e298-128">Új – AzureAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="2e298-128">New-AzureAutomationConnection</span></span>](./New-AzureAutomationConnection.md)

[<span data-ttu-id="2e298-129">Set-AzureAutomationConnectionFieldValue</span><span class="sxs-lookup"><span data-stu-id="2e298-129">Set-AzureAutomationConnectionFieldValue</span></span>](./Set-AzureAutomationConnectionFieldValue.md)


