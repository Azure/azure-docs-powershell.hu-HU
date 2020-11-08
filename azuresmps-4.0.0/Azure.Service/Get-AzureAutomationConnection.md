---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: DD881317-7366-4B55-B1CC-6AF0286F1C5D
online version: ''
schema: 2.0.0
ms.openlocfilehash: 69ef6fc78280180a3722492e5a4b53a52c7bde2a
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016370"
---
# <span data-ttu-id="8487a-101">Get-AzureAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="8487a-101">Get-AzureAutomationConnection</span></span>

## <span data-ttu-id="8487a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="8487a-102">SYNOPSIS</span></span>

<span data-ttu-id="8487a-103">Azure automatizálási kapcsolatot kap.</span><span class="sxs-lookup"><span data-stu-id="8487a-103">Gets an Azure Automation connection.</span></span>

## <span data-ttu-id="8487a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="8487a-104">SYNTAX</span></span>

### <span data-ttu-id="8487a-105">ByAll (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="8487a-105">ByAll (Default)</span></span>
```
Get-AzureAutomationConnection -AutomationAccountName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="8487a-106">ByConnectionName</span><span class="sxs-lookup"><span data-stu-id="8487a-106">ByConnectionName</span></span>
```
Get-AzureAutomationConnection -Name <String> -AutomationAccountName <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="8487a-107">ByConnectionTypeName</span><span class="sxs-lookup"><span data-stu-id="8487a-107">ByConnectionTypeName</span></span>
```
Get-AzureAutomationConnection -ConnectionTypeName <String> -AutomationAccountName <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="8487a-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="8487a-108">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="8487a-109">A **Get-AzureAutomationConnection** parancsmag egy vagy több Microsoft Azure automatizálási kapcsolatot kap.</span><span class="sxs-lookup"><span data-stu-id="8487a-109">The **Get-AzureAutomationConnection** cmdlet gets one or more Microsoft Azure Automation connections.</span></span>
<span data-ttu-id="8487a-110">Alapértelmezés szerint minden kapcsolat visszaadva van.</span><span class="sxs-lookup"><span data-stu-id="8487a-110">By default, all connections are returned.</span></span>
<span data-ttu-id="8487a-111">Ha meghatározott kapcsolatot szeretne kapni, adja meg a nevét.</span><span class="sxs-lookup"><span data-stu-id="8487a-111">To get a specific connection, specify its name.</span></span>
<span data-ttu-id="8487a-112">Ha egy bizonyos típus minden kapcsolatát meg szeretné kapni, adja meg a kapcsolat típusának nevét.</span><span class="sxs-lookup"><span data-stu-id="8487a-112">To get all connections of a certain type, specify the connection type name.</span></span>

## <span data-ttu-id="8487a-113">Példák</span><span class="sxs-lookup"><span data-stu-id="8487a-113">EXAMPLES</span></span>

### <span data-ttu-id="8487a-114">Példa 1: az összes kapcsolat beolvasása</span><span class="sxs-lookup"><span data-stu-id="8487a-114">Example 1: Get all connections</span></span>
```
PS C:\> Get-AzureAutomationConnection -AutomationAccountName "Contoso17"
```

<span data-ttu-id="8487a-115">Ez a parancs a Contoso17 nevű automatizálási fiók összes kapcsolatát beilleszti.</span><span class="sxs-lookup"><span data-stu-id="8487a-115">This command gets all connections in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="8487a-116">2. példa: egy típus összes kapcsolatának beolvasása</span><span class="sxs-lookup"><span data-stu-id="8487a-116">Example 2: Get all connections of a type</span></span>
```
PS C:\> Get-AzureAutomationConnection -AutomationAccountName "Contoso17" -ConnectionTypeName "Azure"
```

<span data-ttu-id="8487a-117">Ez a parancs minden Azure-kapcsolatot beolvas a Contoso17 nevű automatizálási fiókban.</span><span class="sxs-lookup"><span data-stu-id="8487a-117">This command gets all Azure connections in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="8487a-118">3. példa: kapcsolat kérése</span><span class="sxs-lookup"><span data-stu-id="8487a-118">Example 3: Get a connection</span></span>
```
PS C:\> Get-AzureAutomationConnection -AutomationAccountName "Contoso17" -Name "Azure"
```

<span data-ttu-id="8487a-119">Ez a parancs a kapcsolatom nevű kapcsolatot kapja meg.</span><span class="sxs-lookup"><span data-stu-id="8487a-119">This command gets the connection named MyConnection.</span></span>

## <span data-ttu-id="8487a-120">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="8487a-120">PARAMETERS</span></span>

### <span data-ttu-id="8487a-121">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="8487a-121">-AutomationAccountName</span></span>
<span data-ttu-id="8487a-122">Annak az automatizálási fióknak a nevét adja meg, amelyben a lekérdezni kívánt kapcsolat látható.</span><span class="sxs-lookup"><span data-stu-id="8487a-122">Specifies the name of the automation account with the connection to retrieve.</span></span>

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

### <span data-ttu-id="8487a-123">-ConnectionTypeName</span><span class="sxs-lookup"><span data-stu-id="8487a-123">-ConnectionTypeName</span></span>
<span data-ttu-id="8487a-124">A lekérdezni kívánt kapcsolatok kapcsolati típusának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="8487a-124">Specifies the name of a connection type for the connections to retrieve.</span></span>

```yaml
Type: String
Parameter Sets: ByConnectionTypeName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8487a-125">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="8487a-125">-Name</span></span>
<span data-ttu-id="8487a-126">A lekérdezni kívánt kapcsolat nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="8487a-126">Specifies the name of a connection to retrieve.</span></span>

```yaml
Type: String
Parameter Sets: ByConnectionName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8487a-127">-Profil</span><span class="sxs-lookup"><span data-stu-id="8487a-127">-Profile</span></span>
<span data-ttu-id="8487a-128">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="8487a-128">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="8487a-129">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="8487a-129">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="8487a-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8487a-130">CommonParameters</span></span>
<span data-ttu-id="8487a-131">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="8487a-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8487a-132">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8487a-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8487a-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="8487a-133">INPUTS</span></span>

## <span data-ttu-id="8487a-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8487a-134">OUTPUTS</span></span>

### <span data-ttu-id="8487a-135">Microsoft. Azure. Command. Automation. Model. Connection</span><span class="sxs-lookup"><span data-stu-id="8487a-135">Microsoft.Azure.Commands.Automation.Model.Connection</span></span>

## <span data-ttu-id="8487a-136">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="8487a-136">NOTES</span></span>

## <span data-ttu-id="8487a-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8487a-137">RELATED LINKS</span></span>

[<span data-ttu-id="8487a-138">Új – AzureAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="8487a-138">New-AzureAutomationConnection</span></span>](./New-AzureAutomationConnection.md)

[<span data-ttu-id="8487a-139">Remove-AzureAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="8487a-139">Remove-AzureAutomationConnection</span></span>](./Remove-AzureAutomationConnection.md)

[<span data-ttu-id="8487a-140">Set-AzureAutomationConnectionFieldValue</span><span class="sxs-lookup"><span data-stu-id="8487a-140">Set-AzureAutomationConnectionFieldValue</span></span>](./Set-AzureAutomationConnectionFieldValue.md)


