---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: 47664B13-5D63-4012-80E1-7982C8FE22E1
online version: ''
schema: 2.0.0
ms.openlocfilehash: 20edd29629cb5dbbfa6f3f538d1530e9c0692e6c
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016068"
---
# <span data-ttu-id="56e85-101">Set-AzureAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="56e85-101">Set-AzureAutomationVariable</span></span>

## <span data-ttu-id="56e85-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="56e85-102">SYNOPSIS</span></span>

<span data-ttu-id="56e85-103">Automatizálási változó módosítása</span><span class="sxs-lookup"><span data-stu-id="56e85-103">Modifies an Automation variable.</span></span>

## <span data-ttu-id="56e85-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="56e85-104">SYNTAX</span></span>

### <span data-ttu-id="56e85-105">UpdateVariableValue</span><span class="sxs-lookup"><span data-stu-id="56e85-105">UpdateVariableValue</span></span>
```
Set-AzureAutomationVariable -Name <String> -Encrypted <Boolean> -Value <Object> -AutomationAccountName <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="56e85-106">UpdateVariableDescription</span><span class="sxs-lookup"><span data-stu-id="56e85-106">UpdateVariableDescription</span></span>
```
Set-AzureAutomationVariable -Name <String> -Description <String> -AutomationAccountName <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="56e85-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="56e85-107">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="56e85-108">A **set-AzureAutomationVariable** parancsmag módosítja egy változó értékét vagy leírását a Microsoft Azure automatizálásban.</span><span class="sxs-lookup"><span data-stu-id="56e85-108">The **Set-AzureAutomationVariable** cmdlet modifies the value or description of a variable in Microsoft Azure Automation.</span></span>

## <span data-ttu-id="56e85-109">Példák</span><span class="sxs-lookup"><span data-stu-id="56e85-109">EXAMPLES</span></span>

### <span data-ttu-id="56e85-110">Példa 1: változó értékének beállítása</span><span class="sxs-lookup"><span data-stu-id="56e85-110">Example 1: Set the value of a variable</span></span>
```
PS C:\> Set-AzureAutomationVariable -AutomationAccountName "Contoso17" -Name "MyStringVariable" -Value "New Value" -Encrypted $False
```

<span data-ttu-id="56e85-111">Ez a parancs a MyStringVariable nevű változó új értékét állítja be a Contoso17 nevű Azure automatizálási fiókban.</span><span class="sxs-lookup"><span data-stu-id="56e85-111">This command sets a new value for the variable named MyStringVariable in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="56e85-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="56e85-112">PARAMETERS</span></span>

### <span data-ttu-id="56e85-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="56e85-113">-AutomationAccountName</span></span>
<span data-ttu-id="56e85-114">A változóval rendelkező automatizálási fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="56e85-114">Specifies the name of the Automation account with the variable.</span></span>

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

### <span data-ttu-id="56e85-115">-Leírás</span><span class="sxs-lookup"><span data-stu-id="56e85-115">-Description</span></span>
<span data-ttu-id="56e85-116">A változó leírását adja meg.</span><span class="sxs-lookup"><span data-stu-id="56e85-116">Specifies a description for the variable.</span></span>

```yaml
Type: String
Parameter Sets: UpdateVariableDescription
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="56e85-117">-Titkosított</span><span class="sxs-lookup"><span data-stu-id="56e85-117">-Encrypted</span></span>
<span data-ttu-id="56e85-118">Azt jelzi, hogy titkosítja-e a változót.</span><span class="sxs-lookup"><span data-stu-id="56e85-118">Indicates whether to encrypt the variable.</span></span>

```yaml
Type: Boolean
Parameter Sets: UpdateVariableValue
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="56e85-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="56e85-119">-Name</span></span>
<span data-ttu-id="56e85-120">A változó nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="56e85-120">Specifies the name of the variable.</span></span>

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

### <span data-ttu-id="56e85-121">-Profil</span><span class="sxs-lookup"><span data-stu-id="56e85-121">-Profile</span></span>
<span data-ttu-id="56e85-122">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="56e85-122">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="56e85-123">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="56e85-123">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="56e85-124">-Value (érték)</span><span class="sxs-lookup"><span data-stu-id="56e85-124">-Value</span></span>
<span data-ttu-id="56e85-125">A változó értékét adja meg.</span><span class="sxs-lookup"><span data-stu-id="56e85-125">Specifies a value for the variable.</span></span>

```yaml
Type: Object
Parameter Sets: UpdateVariableValue
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="56e85-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="56e85-126">CommonParameters</span></span>
<span data-ttu-id="56e85-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="56e85-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="56e85-128">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="56e85-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="56e85-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="56e85-129">INPUTS</span></span>

## <span data-ttu-id="56e85-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="56e85-130">OUTPUTS</span></span>

### <span data-ttu-id="56e85-131">Microsoft. Azure. Command. Automation. Model. változó</span><span class="sxs-lookup"><span data-stu-id="56e85-131">Microsoft.Azure.Commands.Automation.Model.Variable</span></span>

## <span data-ttu-id="56e85-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="56e85-132">NOTES</span></span>

## <span data-ttu-id="56e85-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="56e85-133">RELATED LINKS</span></span>

[<span data-ttu-id="56e85-134">Get-AzureAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="56e85-134">Get-AzureAutomationVariable</span></span>](./Get-AzureAutomationVariable.md)

[<span data-ttu-id="56e85-135">Új – AzureAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="56e85-135">New-AzureAutomationVariable</span></span>](./New-AzureAutomationVariable.md)

[<span data-ttu-id="56e85-136">Remove-AzureAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="56e85-136">Remove-AzureAutomationVariable</span></span>](./Remove-AzureAutomationVariable.md)


