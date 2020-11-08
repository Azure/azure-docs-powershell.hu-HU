---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: C92B4B70-4342-4219-80D3-FB79BDC171A3
online version: ''
schema: 2.0.0
ms.openlocfilehash: 16fbdf1a0a63fb5a75aa7bc200036a7332ea15f8
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015831"
---
# <span data-ttu-id="cf66c-101">Set-AzureAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="cf66c-101">Set-AzureAutomationCredential</span></span>

## <span data-ttu-id="cf66c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="cf66c-102">SYNOPSIS</span></span>

<span data-ttu-id="cf66c-103">A hitelesítő adatok módosítása az automatizálásban.</span><span class="sxs-lookup"><span data-stu-id="cf66c-103">Modifies a credential in Automation.</span></span>

## <span data-ttu-id="cf66c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="cf66c-104">SYNTAX</span></span>

```
Set-AzureAutomationCredential -Name <String> [-Description <String>] [-Value <PSCredential>]
 -AutomationAccountName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="cf66c-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="cf66c-105">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="cf66c-106">A **set-AzureAutomationCredential** parancsmag **PSCredential** -objektumként módosítja a hitelesítő adatokat a Microsoft Azure automatizálási szolgáltatásban.</span><span class="sxs-lookup"><span data-stu-id="cf66c-106">The **Set-AzureAutomationCredential** cmdlet modifies a credential as a **PSCredential** object in Microsoft Azure Automation.</span></span>

## <span data-ttu-id="cf66c-107">Példák</span><span class="sxs-lookup"><span data-stu-id="cf66c-107">EXAMPLES</span></span>

### <span data-ttu-id="cf66c-108">Példa 1: hitelesítő adatok frissítése</span><span class="sxs-lookup"><span data-stu-id="cf66c-108">Example 1: Update a credential</span></span>
```
PS C:\> $user = "MyDomain\MyUser"
PS C:\> $pw = ConvertTo-SecureString "PassWord!" -AsPlainText -Force
PS C:\> $cred = New-Object -TypeName System.Management.Automation.PSCredential -ArgumentList $user, $pw
PS C:\> New-AzureAutomationCredential -AutomationAccountName "Contos17" -Name "MyCredential" -Value $cred
```

<span data-ttu-id="cf66c-109">Ezek a parancsok frissítik a MyCredential nevű meglévő hitelesítő adatokat.</span><span class="sxs-lookup"><span data-stu-id="cf66c-109">These commands update an existing credential named MyCredential.</span></span>
<span data-ttu-id="cf66c-110">Először létrejön egy hitelesítőadat-objektum, amely tartalmazza a felhasználónevet és a jelszót.</span><span class="sxs-lookup"><span data-stu-id="cf66c-110">A credential object is first created that includes a username and password.</span></span>
<span data-ttu-id="cf66c-111">Ezt követően a rendszer az utolsó parancsban használja az automatizálási hitelesítő adatok frissítését.</span><span class="sxs-lookup"><span data-stu-id="cf66c-111">This is then used in the last command to update the automation credential.</span></span>

## <span data-ttu-id="cf66c-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="cf66c-112">PARAMETERS</span></span>

### <span data-ttu-id="cf66c-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="cf66c-113">-AutomationAccountName</span></span>
<span data-ttu-id="cf66c-114">A hitelesítő adatokkal rendelkező automatizálási fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="cf66c-114">Specifies the name of the Automation account with the credential.</span></span>

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

### <span data-ttu-id="cf66c-115">-Leírás</span><span class="sxs-lookup"><span data-stu-id="cf66c-115">-Description</span></span>
<span data-ttu-id="cf66c-116">A hitelesítő adatok leírását adja meg.</span><span class="sxs-lookup"><span data-stu-id="cf66c-116">Specifies a description for the credential.</span></span>

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

### <span data-ttu-id="cf66c-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="cf66c-117">-Name</span></span>
<span data-ttu-id="cf66c-118">A hitelesítő adatok nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="cf66c-118">Specifies the name of the credential.</span></span>

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

### <span data-ttu-id="cf66c-119">-Profil</span><span class="sxs-lookup"><span data-stu-id="cf66c-119">-Profile</span></span>
<span data-ttu-id="cf66c-120">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="cf66c-120">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="cf66c-121">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="cf66c-121">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="cf66c-122">-Value (érték)</span><span class="sxs-lookup"><span data-stu-id="cf66c-122">-Value</span></span>
<span data-ttu-id="cf66c-123">A hitelesítő adatokat **PSCredential** -objektumként adja meg.</span><span class="sxs-lookup"><span data-stu-id="cf66c-123">Specifies the credentials as a **PSCredential** object.</span></span>

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cf66c-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cf66c-124">CommonParameters</span></span>
<span data-ttu-id="cf66c-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="cf66c-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cf66c-126">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cf66c-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cf66c-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="cf66c-127">INPUTS</span></span>

## <span data-ttu-id="cf66c-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="cf66c-128">OUTPUTS</span></span>

### <span data-ttu-id="cf66c-129">Microsoft. Azure. Command. Automation. Model. CredentialInfo</span><span class="sxs-lookup"><span data-stu-id="cf66c-129">Microsoft.Azure.Commands.Automation.Model.CredentialInfo</span></span>

## <span data-ttu-id="cf66c-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="cf66c-130">NOTES</span></span>

## <span data-ttu-id="cf66c-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="cf66c-131">RELATED LINKS</span></span>

[<span data-ttu-id="cf66c-132">Get-AzureAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="cf66c-132">Get-AzureAutomationCredential</span></span>](./Get-AzureAutomationCredential.md)

[<span data-ttu-id="cf66c-133">Új – AzureAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="cf66c-133">New-AzureAutomationCredential</span></span>](./New-AzureAutomationCredential.md)

[<span data-ttu-id="cf66c-134">Remove-AzureAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="cf66c-134">Remove-AzureAutomationCredential</span></span>](./Remove-AzureAutomationCredential.md)


