---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: D88C6B17-5D0E-4E23-9C5C-DB38DED9061C
online version: ''
schema: 2.0.0
ms.openlocfilehash: 1518c351a67c84e6dacafd1fa8a394051f3bfeac
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015931"
---
# <span data-ttu-id="76bfb-101">New-AzureAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="76bfb-101">New-AzureAutomationVariable</span></span>

## <span data-ttu-id="76bfb-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="76bfb-102">SYNOPSIS</span></span>

<span data-ttu-id="76bfb-103">Automatizálási változót hoz létre.</span><span class="sxs-lookup"><span data-stu-id="76bfb-103">Creates an Automation variable.</span></span>

## <span data-ttu-id="76bfb-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="76bfb-104">SYNTAX</span></span>

```
New-AzureAutomationVariable -Name <String> -Encrypted <Boolean> [-Description <String>] [-Value <Object>]
 -AutomationAccountName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="76bfb-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="76bfb-105">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="76bfb-106">A **New-AzureAutomationVariable** parancsmag változót hoz létre a Microsoft Azure automatizálásban.</span><span class="sxs-lookup"><span data-stu-id="76bfb-106">The **New-AzureAutomationVariable** cmdlet creates a variable in Microsoft Azure Automation.</span></span>

## <span data-ttu-id="76bfb-107">Példák</span><span class="sxs-lookup"><span data-stu-id="76bfb-107">EXAMPLES</span></span>

### <span data-ttu-id="76bfb-108">Példa 1: új változó létrehozása egyszerű értékkel</span><span class="sxs-lookup"><span data-stu-id="76bfb-108">Example 1: Create a new variable with a simple value</span></span>
```
PS C:\> New-AzureAutomationVariable -AutomationAccountName "Contoso17" -Name "MyStringVariable" -Encrypted $False -Value "My String"
```

<span data-ttu-id="76bfb-109">Ez a parancs létrehoz egy MyStringVariable nevű új változót egy karakterlánc értékkel az Contoso17 nevű Azure automatizálási fiókban.</span><span class="sxs-lookup"><span data-stu-id="76bfb-109">This command creates a new variable named MyStringVariable with a string value in the Azure Automation account named Contoso17.</span></span>

### <span data-ttu-id="76bfb-110">2. példa: új változó létrehozása komplex értékkel</span><span class="sxs-lookup"><span data-stu-id="76bfb-110">Example 2: Create a new variable with a complex value</span></span>
```
PS C:\> $vm = Get-AzureVM -ServiceName "MyVM" -Name "MyVM"
PS C:\> New-AzureAutomationVariable -AutomationAccountName "Contoso17" -Name "MyComplexVariable" -Encrypted $False -Value $vm
```

<span data-ttu-id="76bfb-111">Ezekkel a parancsokkal új változót hozhat létre a MyComplexVariable nevű Contoso17 nevű automatizálási fiókban.</span><span class="sxs-lookup"><span data-stu-id="76bfb-111">These commands create a new variable called MyComplexVariable in the Automation account named Contoso17.</span></span>
<span data-ttu-id="76bfb-112">Az értékhez egy komplex objektum van használatban, ebben az esetben egy virtuális gép objektum.</span><span class="sxs-lookup"><span data-stu-id="76bfb-112">A complex object is used for its value, in this case a virtual machine object.</span></span>

## <span data-ttu-id="76bfb-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="76bfb-113">PARAMETERS</span></span>

### <span data-ttu-id="76bfb-114">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="76bfb-114">-AutomationAccountName</span></span>
<span data-ttu-id="76bfb-115">Annak az automatizálási fióknak a nevét adja meg, amelyben a változót tárolják.</span><span class="sxs-lookup"><span data-stu-id="76bfb-115">Specifies the name of the Automation account the variable will be stored in.</span></span>

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

### <span data-ttu-id="76bfb-116">-Leírás</span><span class="sxs-lookup"><span data-stu-id="76bfb-116">-Description</span></span>
<span data-ttu-id="76bfb-117">A változó leírását adja meg.</span><span class="sxs-lookup"><span data-stu-id="76bfb-117">Specifies a description for the variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="76bfb-118">-Titkosított</span><span class="sxs-lookup"><span data-stu-id="76bfb-118">-Encrypted</span></span>
<span data-ttu-id="76bfb-119">Azt jelzi, hogy a változó értékét titkosítva kell-e tárolni.</span><span class="sxs-lookup"><span data-stu-id="76bfb-119">Indicates whether the value of the variable should be stored encrypted.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="76bfb-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="76bfb-120">-Name</span></span>
<span data-ttu-id="76bfb-121">A változó nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="76bfb-121">Specifies a name for the variable.</span></span>

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

### <span data-ttu-id="76bfb-122">-Profil</span><span class="sxs-lookup"><span data-stu-id="76bfb-122">-Profile</span></span>
<span data-ttu-id="76bfb-123">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="76bfb-123">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="76bfb-124">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="76bfb-124">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="76bfb-125">-Value (érték)</span><span class="sxs-lookup"><span data-stu-id="76bfb-125">-Value</span></span>
<span data-ttu-id="76bfb-126">A változóban tárolandó értéket adja meg.</span><span class="sxs-lookup"><span data-stu-id="76bfb-126">Specifies a value to store in the variable.</span></span>

```yaml
Type: Object
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="76bfb-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="76bfb-127">CommonParameters</span></span>
<span data-ttu-id="76bfb-128">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="76bfb-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="76bfb-129">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="76bfb-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="76bfb-130">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="76bfb-130">INPUTS</span></span>

## <span data-ttu-id="76bfb-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="76bfb-131">OUTPUTS</span></span>

### <span data-ttu-id="76bfb-132">Microsoft. Azure. Command. Automation. Model. változó</span><span class="sxs-lookup"><span data-stu-id="76bfb-132">Microsoft.Azure.Commands.Automation.Model.Variable</span></span>

## <span data-ttu-id="76bfb-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="76bfb-133">NOTES</span></span>

## <span data-ttu-id="76bfb-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="76bfb-134">RELATED LINKS</span></span>

[<span data-ttu-id="76bfb-135">Get-AzureAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="76bfb-135">Get-AzureAutomationVariable</span></span>](./Get-AzureAutomationVariable.md)

[<span data-ttu-id="76bfb-136">Remove-AzureAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="76bfb-136">Remove-AzureAutomationVariable</span></span>](./Remove-AzureAutomationVariable.md)

[<span data-ttu-id="76bfb-137">Set-AzureAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="76bfb-137">Set-AzureAutomationVariable</span></span>](./Set-AzureAutomationVariable.md)


