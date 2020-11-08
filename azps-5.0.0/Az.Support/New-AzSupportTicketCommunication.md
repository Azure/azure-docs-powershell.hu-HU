---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Support.dll-Help.xml
Module Name: Az.Support
online version: https://docs.microsoft.com/en-us/powershell/module/az.support/new-azsupportticketcommunication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/New-AzSupportTicketCommunication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/New-AzSupportTicketCommunication.md
ms.openlocfilehash: 3a0191e1df223427ec7d60dfd92f7607e2c171b0
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94187920"
---
# <span data-ttu-id="21d7b-101">New-AzSupportTicketCommunication</span><span class="sxs-lookup"><span data-stu-id="21d7b-101">New-AzSupportTicketCommunication</span></span>

## <span data-ttu-id="21d7b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="21d7b-102">SYNOPSIS</span></span>
<span data-ttu-id="21d7b-103">Új támogatási jegyet tartalmazó kommunikáció létrehozása.</span><span class="sxs-lookup"><span data-stu-id="21d7b-103">Creates a new support ticket communication.</span></span>

## <span data-ttu-id="21d7b-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="21d7b-104">SYNTAX</span></span>

### <span data-ttu-id="21d7b-105">CreateByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="21d7b-105">CreateByNameParameterSet (Default)</span></span>
```
New-AzSupportTicketCommunication -SupportTicketName <String> -Name <String> -Subject <String> -Body <String>
 [-Sender <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="21d7b-106">CreateByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="21d7b-106">CreateByParentObjectParameterSet</span></span>
```
New-AzSupportTicketCommunication -SupportTicketObject <PSSupportTicket> -Name <String> -Subject <String>
 -Body <String> [-Sender <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="21d7b-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="21d7b-107">DESCRIPTION</span></span>
<span data-ttu-id="21d7b-108">Új ügyfél-kommunikációt ad az Azure támogatási jegyéhez.</span><span class="sxs-lookup"><span data-stu-id="21d7b-108">Adds a new customer communication to an Azure support ticket.</span></span>

## <span data-ttu-id="21d7b-109">Példák</span><span class="sxs-lookup"><span data-stu-id="21d7b-109">EXAMPLES</span></span>

### <span data-ttu-id="21d7b-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="21d7b-110">Example 1</span></span>
```powershell
PS C:\> New-AzSupportTicketCommunication -Name "testmessage" -SupportTicketName "testticket" -Subject "test subject" -Body "test body" -Sender "user@contoso.com"

Name         Sender               Subject        CreatedDate
----         ------               -------        -----------
testmessage  user@contoso.com     test subject   2/4/2020 9:38:14 PM
```

## <span data-ttu-id="21d7b-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="21d7b-111">PARAMETERS</span></span>

### <span data-ttu-id="21d7b-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="21d7b-112">-AsJob</span></span>
<span data-ttu-id="21d7b-113">Futtassa a parancsmagot a háttérben.</span><span class="sxs-lookup"><span data-stu-id="21d7b-113">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="21d7b-114">-Body</span><span class="sxs-lookup"><span data-stu-id="21d7b-114">-Body</span></span>
<span data-ttu-id="21d7b-115">A kommunikáció törzse</span><span class="sxs-lookup"><span data-stu-id="21d7b-115">Body of the communication.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21d7b-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="21d7b-116">-DefaultProfile</span></span>
<span data-ttu-id="21d7b-117">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="21d7b-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="21d7b-118">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="21d7b-118">-Name</span></span>
<span data-ttu-id="21d7b-119">A kommunikációs erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="21d7b-119">Name of the communication resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21d7b-120">-Feladó</span><span class="sxs-lookup"><span data-stu-id="21d7b-120">-Sender</span></span>
<span data-ttu-id="21d7b-121">A feladó e-mail-címe.</span><span class="sxs-lookup"><span data-stu-id="21d7b-121">Email address of the sender.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21d7b-122">-Tárgy</span><span class="sxs-lookup"><span data-stu-id="21d7b-122">-Subject</span></span>
<span data-ttu-id="21d7b-123">A kommunikáció tárgya.</span><span class="sxs-lookup"><span data-stu-id="21d7b-123">Subject of the communication.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21d7b-124">-SupportTicketName</span><span class="sxs-lookup"><span data-stu-id="21d7b-124">-SupportTicketName</span></span>
<span data-ttu-id="21d7b-125">Támogatási jegy neve</span><span class="sxs-lookup"><span data-stu-id="21d7b-125">Support ticket name.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21d7b-126">-SupportTicketObject</span><span class="sxs-lookup"><span data-stu-id="21d7b-126">-SupportTicketObject</span></span>
<span data-ttu-id="21d7b-127">Támogatási jegy objektum.</span><span class="sxs-lookup"><span data-stu-id="21d7b-127">Support ticket object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Support.Models.PSSupportTicket
Parameter Sets: CreateByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="21d7b-128">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="21d7b-128">-Confirm</span></span>
<span data-ttu-id="21d7b-129">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="21d7b-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21d7b-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="21d7b-130">-WhatIf</span></span>
<span data-ttu-id="21d7b-131">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="21d7b-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="21d7b-132">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="21d7b-132">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21d7b-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="21d7b-133">CommonParameters</span></span>
<span data-ttu-id="21d7b-134">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="21d7b-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="21d7b-135">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="21d7b-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="21d7b-136">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="21d7b-136">INPUTS</span></span>

### <span data-ttu-id="21d7b-137">Microsoft. Azure. commands. support. models. PSSupportTicket</span><span class="sxs-lookup"><span data-stu-id="21d7b-137">Microsoft.Azure.Commands.Support.Models.PSSupportTicket</span></span>

## <span data-ttu-id="21d7b-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="21d7b-138">OUTPUTS</span></span>

### <span data-ttu-id="21d7b-139">Microsoft. Azure. commands. support. models. PSSupportTicketCommunication</span><span class="sxs-lookup"><span data-stu-id="21d7b-139">Microsoft.Azure.Commands.Support.Models.PSSupportTicketCommunication</span></span>

## <span data-ttu-id="21d7b-140">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="21d7b-140">NOTES</span></span>

## <span data-ttu-id="21d7b-141">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="21d7b-141">RELATED LINKS</span></span>
