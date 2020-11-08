---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: B7E71C5C-6329-475B-993C-A839FFEF8F98
online version: ''
schema: 2.0.0
ms.openlocfilehash: cef5d19cdb954e98fe0e97cc0042bfaf91505c0c
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016220"
---
# <span data-ttu-id="21e03-101">New-AzureAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="21e03-101">New-AzureAutomationConnection</span></span>

## <span data-ttu-id="21e03-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="21e03-102">SYNOPSIS</span></span>

<span data-ttu-id="21e03-103">Kapcsolatot létesít az automatizálásban.</span><span class="sxs-lookup"><span data-stu-id="21e03-103">Creates a connection in Automation.</span></span>

## <span data-ttu-id="21e03-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="21e03-104">SYNTAX</span></span>

```
New-AzureAutomationConnection -Name <String> -ConnectionTypeName <String> -ConnectionFieldValues <IDictionary>
 [-Description <String>] -AutomationAccountName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="21e03-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="21e03-105">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="21e03-106">A **New-AzureAutomationConnection** parancsmag kapcsolatot létesít a Microsoft Azure automatizálási szolgáltatással.</span><span class="sxs-lookup"><span data-stu-id="21e03-106">The **New-AzureAutomationConnection** cmdlet creates a connection in Microsoft Azure Automation.</span></span>

## <span data-ttu-id="21e03-107">Példák</span><span class="sxs-lookup"><span data-stu-id="21e03-107">EXAMPLES</span></span>

## <span data-ttu-id="21e03-108">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="21e03-108">PARAMETERS</span></span>

### <span data-ttu-id="21e03-109">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="21e03-109">-AutomationAccountName</span></span>
<span data-ttu-id="21e03-110">Annak az automatizálási fióknak a neve, amelyet a rendszer a kapcsolaton tárol.</span><span class="sxs-lookup"><span data-stu-id="21e03-110">Specifies the name of the Automation account the connection will be stored in.</span></span>

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

### <span data-ttu-id="21e03-111">-ConnectionFieldValues</span><span class="sxs-lookup"><span data-stu-id="21e03-111">-ConnectionFieldValues</span></span>
<span data-ttu-id="21e03-112">Egy kulcs/érték párokat tartalmazó kivonatoló táblát ad meg.</span><span class="sxs-lookup"><span data-stu-id="21e03-112">Specifies a hash table that contains key/value pairs.</span></span>
<span data-ttu-id="21e03-113">A kulcsok a megadott kapcsolattípus kapcsolat mezőit jelzik.</span><span class="sxs-lookup"><span data-stu-id="21e03-113">The keys represent the connection fields on the specified connection type.</span></span>
<span data-ttu-id="21e03-114">Az értékek a csatlakozási példány minden egyes kapcsolat mezőjében tárolható meghatározott értékeket jelentik.</span><span class="sxs-lookup"><span data-stu-id="21e03-114">The values represent the specific values to store for each connection field for the connection instance.</span></span>

```yaml
Type: IDictionary
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="21e03-115">-ConnectionTypeName</span><span class="sxs-lookup"><span data-stu-id="21e03-115">-ConnectionTypeName</span></span>
<span data-ttu-id="21e03-116">A kapcsolat típusának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="21e03-116">Specifies the name of the connection type.</span></span>

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

### <span data-ttu-id="21e03-117">-Leírás</span><span class="sxs-lookup"><span data-stu-id="21e03-117">-Description</span></span>
<span data-ttu-id="21e03-118">A hitelesítő adatok leírását adja meg.</span><span class="sxs-lookup"><span data-stu-id="21e03-118">Specifies a description for the credential.</span></span>

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

### <span data-ttu-id="21e03-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="21e03-119">-Name</span></span>
<span data-ttu-id="21e03-120">A kapcsolat nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="21e03-120">Specifies a name for the connection.</span></span>

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

### <span data-ttu-id="21e03-121">-Profil</span><span class="sxs-lookup"><span data-stu-id="21e03-121">-Profile</span></span>
<span data-ttu-id="21e03-122">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="21e03-122">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="21e03-123">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="21e03-123">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="21e03-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="21e03-124">CommonParameters</span></span>
<span data-ttu-id="21e03-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="21e03-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="21e03-126">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="21e03-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="21e03-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="21e03-127">INPUTS</span></span>

## <span data-ttu-id="21e03-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="21e03-128">OUTPUTS</span></span>

### <span data-ttu-id="21e03-129">Microsoft. Azure. Command. Automation. Model. Connection</span><span class="sxs-lookup"><span data-stu-id="21e03-129">Microsoft.Azure.Commands.Automation.Model.Connection</span></span>

## <span data-ttu-id="21e03-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="21e03-130">NOTES</span></span>

## <span data-ttu-id="21e03-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="21e03-131">RELATED LINKS</span></span>

[<span data-ttu-id="21e03-132">Get-AzureAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="21e03-132">Get-AzureAutomationConnection</span></span>](./Get-AzureAutomationConnection.md)

[<span data-ttu-id="21e03-133">Remove-AzureAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="21e03-133">Remove-AzureAutomationConnection</span></span>](./Remove-AzureAutomationConnection.md)

[<span data-ttu-id="21e03-134">Set-AzureAutomationConnectionFieldValue</span><span class="sxs-lookup"><span data-stu-id="21e03-134">Set-AzureAutomationConnectionFieldValue</span></span>](./Set-AzureAutomationConnectionFieldValue.md)


