---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: C69558DB-78C3-4162-99C3-1300C3FE5287
online version: ''
schema: 2.0.0
ms.openlocfilehash: aa73cf467ffc3675b17b6c59ef5bd07483803267
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015659"
---
# <span data-ttu-id="6d47d-101">Get-AzureAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="6d47d-101">Get-AzureAutomationCredential</span></span>

## <span data-ttu-id="6d47d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="6d47d-102">SYNOPSIS</span></span>

<span data-ttu-id="6d47d-103">Azure Automation hitelesítő adatokat kap.</span><span class="sxs-lookup"><span data-stu-id="6d47d-103">Gets an Azure Automation credential.</span></span>

## <span data-ttu-id="6d47d-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="6d47d-104">SYNTAX</span></span>

### <span data-ttu-id="6d47d-105">ByAll (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="6d47d-105">ByAll (Default)</span></span>
```
Get-AzureAutomationCredential -AutomationAccountName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="6d47d-106">ByName</span><span class="sxs-lookup"><span data-stu-id="6d47d-106">ByName</span></span>
```
Get-AzureAutomationCredential -Name <String> -AutomationAccountName <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="6d47d-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="6d47d-107">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="6d47d-108">A **Get-AzureAutomationCredential** parancsmag egy vagy több Microsoft Azure automatizálási hitelesítő adatokat kap.</span><span class="sxs-lookup"><span data-stu-id="6d47d-108">The **Get-AzureAutomationCredential** cmdlet gets one or more Microsoft Azure Automation credentials.</span></span>
<span data-ttu-id="6d47d-109">Alapértelmezés szerint minden hitelesítő adatot visszaad a rendszer.</span><span class="sxs-lookup"><span data-stu-id="6d47d-109">By default, all credentials are returned.</span></span>
<span data-ttu-id="6d47d-110">A megadott hitelesítő adatok megadásához adja meg a nevét.</span><span class="sxs-lookup"><span data-stu-id="6d47d-110">To get a specific credential, specify its name.</span></span>

## <span data-ttu-id="6d47d-111">Példák</span><span class="sxs-lookup"><span data-stu-id="6d47d-111">EXAMPLES</span></span>

### <span data-ttu-id="6d47d-112">Példa 1: a hitelesítő adatok beszerzése</span><span class="sxs-lookup"><span data-stu-id="6d47d-112">Example 1: Get all credentials</span></span>
```
PS C:\> Get-AzureAutomationCredential -AutomationAccountName "Contoso17"
```

<span data-ttu-id="6d47d-113">Ez a parancs a Contoso17 nevű automatizálási fiók minden hitelesítő adatait beolvassa.</span><span class="sxs-lookup"><span data-stu-id="6d47d-113">This command gets all credentials in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="6d47d-114">2. példa: hitelesítő adatok beszerzése</span><span class="sxs-lookup"><span data-stu-id="6d47d-114">Example 2: Get a credential</span></span>
```
PS C:\> Get-AzureAutomationCredential -AutomationAccountName "Contoso17" -Name "MyCredential"
```

<span data-ttu-id="6d47d-115">Ez a parancs a MyCredential nevű hitelesítő adatokat kapja meg.</span><span class="sxs-lookup"><span data-stu-id="6d47d-115">This command gets the credential named MyCredential.</span></span>

## <span data-ttu-id="6d47d-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="6d47d-116">PARAMETERS</span></span>

### <span data-ttu-id="6d47d-117">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="6d47d-117">-AutomationAccountName</span></span>
<span data-ttu-id="6d47d-118">Az automatizálási fiók nevét adja meg a beolvasandó hitelesítő adatokkal.</span><span class="sxs-lookup"><span data-stu-id="6d47d-118">Specifies the name of the automation account with the credential to retrieve.</span></span>

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

### <span data-ttu-id="6d47d-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="6d47d-119">-Name</span></span>
<span data-ttu-id="6d47d-120">A lekérdezni kívánt hitelesítő adatok nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="6d47d-120">Specifies the name of a credential to retrieve.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6d47d-121">-Profil</span><span class="sxs-lookup"><span data-stu-id="6d47d-121">-Profile</span></span>
<span data-ttu-id="6d47d-122">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="6d47d-122">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="6d47d-123">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="6d47d-123">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="6d47d-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6d47d-124">CommonParameters</span></span>
<span data-ttu-id="6d47d-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="6d47d-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6d47d-126">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6d47d-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6d47d-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="6d47d-127">INPUTS</span></span>

## <span data-ttu-id="6d47d-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6d47d-128">OUTPUTS</span></span>

### <span data-ttu-id="6d47d-129">Microsoft. Azure. Command. Automation. Model. CredentialInfo</span><span class="sxs-lookup"><span data-stu-id="6d47d-129">Microsoft.Azure.Commands.Automation.Model.CredentialInfo</span></span>

## <span data-ttu-id="6d47d-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="6d47d-130">NOTES</span></span>

## <span data-ttu-id="6d47d-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6d47d-131">RELATED LINKS</span></span>

[<span data-ttu-id="6d47d-132">Új – AzureAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="6d47d-132">New-AzureAutomationCredential</span></span>](./New-AzureAutomationCredential.md)

[<span data-ttu-id="6d47d-133">Remove-AzureAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="6d47d-133">Remove-AzureAutomationCredential</span></span>](./Remove-AzureAutomationCredential.md)

[<span data-ttu-id="6d47d-134">Set-AzureAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="6d47d-134">Set-AzureAutomationCredential</span></span>](./Set-AzureAutomationCredential.md)


