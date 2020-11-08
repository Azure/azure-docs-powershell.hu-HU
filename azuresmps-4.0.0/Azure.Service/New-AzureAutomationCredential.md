---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: E42F05D0-28AD-4772-9F53-BCE6EFC698AF
online version: ''
schema: 2.0.0
ms.openlocfilehash: bc7d44b87c1e371f0d0c065746dae991cff1cca8
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016221"
---
# <span data-ttu-id="cde5d-101">New-AzureAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="cde5d-101">New-AzureAutomationCredential</span></span>

## <span data-ttu-id="cde5d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="cde5d-102">SYNOPSIS</span></span>

<span data-ttu-id="cde5d-103">Hitelesítő adatokat hoz létre az automatizálásban.</span><span class="sxs-lookup"><span data-stu-id="cde5d-103">Creates a credential in Automation.</span></span>

## <span data-ttu-id="cde5d-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="cde5d-104">SYNTAX</span></span>

```
New-AzureAutomationCredential -Name <String> [-Description <String>] -Value <PSCredential>
 -AutomationAccountName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="cde5d-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="cde5d-105">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="cde5d-106">A **New-AzureAutomationCredential** parancsmag **PSCredential** -objektumként hozza létre a hitelesítő adatait a Microsoft Azure automatizálásban.</span><span class="sxs-lookup"><span data-stu-id="cde5d-106">The **New-AzureAutomationCredential** cmdlet creates a credential as a **PSCredential** object in Microsoft Azure Automation.</span></span>

## <span data-ttu-id="cde5d-107">Példák</span><span class="sxs-lookup"><span data-stu-id="cde5d-107">EXAMPLES</span></span>

### <span data-ttu-id="cde5d-108">Példa 1: hitelesítő adatok létrehozása</span><span class="sxs-lookup"><span data-stu-id="cde5d-108">Example 1: Create a credential</span></span>
```
PS C:\> $user = "MyDomain\MyUser"
PS C:\> $pw = ConvertTo-SecureString "PassWord!" -AsPlainText -Force
PS C:\> $cred = New-Object -TypeName System.Management.Automation.PSCredential -ArgumentList $user, $pw
PS C:\> New-AzureAutomationCredential -AutomationAccountName "Contoso17" -Name "MyCredential" -Value $cred
```

<span data-ttu-id="cde5d-109">Ezekkel a parancsokkal létrehozhatja a MyCredential nevű hitelesítő adatokat.</span><span class="sxs-lookup"><span data-stu-id="cde5d-109">These commands create a credential named MyCredential.</span></span>
<span data-ttu-id="cde5d-110">Először létrejön egy hitelesítőadat-objektum, amely tartalmazza a felhasználónevet és a jelszót.</span><span class="sxs-lookup"><span data-stu-id="cde5d-110">A credential object is first created that includes a username and password.</span></span>
<span data-ttu-id="cde5d-111">Ezt követően a rendszer az utolsó parancsban használja az automatizálási hitelesítő adatok létrehozását.</span><span class="sxs-lookup"><span data-stu-id="cde5d-111">This is then used in the last command to create the Automation credential.</span></span>

## <span data-ttu-id="cde5d-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="cde5d-112">PARAMETERS</span></span>

### <span data-ttu-id="cde5d-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="cde5d-113">-AutomationAccountName</span></span>
<span data-ttu-id="cde5d-114">Annak az automatizálási fióknak a nevét adja meg, amelyre a hitelesítő adatok lesznek tárolva.</span><span class="sxs-lookup"><span data-stu-id="cde5d-114">Specifies the name of the Automation account the credential will be stored in.</span></span>

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

### <span data-ttu-id="cde5d-115">-Leírás</span><span class="sxs-lookup"><span data-stu-id="cde5d-115">-Description</span></span>
<span data-ttu-id="cde5d-116">A hitelesítő adatok leírását adja meg.</span><span class="sxs-lookup"><span data-stu-id="cde5d-116">Specifies a description for the credential.</span></span>

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

### <span data-ttu-id="cde5d-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="cde5d-117">-Name</span></span>
<span data-ttu-id="cde5d-118">A hitelesítő adatok nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="cde5d-118">Specifies a name for the credential.</span></span>

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

### <span data-ttu-id="cde5d-119">-Profil</span><span class="sxs-lookup"><span data-stu-id="cde5d-119">-Profile</span></span>
<span data-ttu-id="cde5d-120">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="cde5d-120">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="cde5d-121">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="cde5d-121">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="cde5d-122">-Value (érték)</span><span class="sxs-lookup"><span data-stu-id="cde5d-122">-Value</span></span>
<span data-ttu-id="cde5d-123">A hitelesítő adatokat **PSCredential** -objektumként adja meg.</span><span class="sxs-lookup"><span data-stu-id="cde5d-123">Specifies the credentials as a **PSCredential** object.</span></span>

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cde5d-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cde5d-124">CommonParameters</span></span>
<span data-ttu-id="cde5d-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="cde5d-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cde5d-126">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cde5d-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cde5d-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="cde5d-127">INPUTS</span></span>

## <span data-ttu-id="cde5d-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="cde5d-128">OUTPUTS</span></span>

### <span data-ttu-id="cde5d-129">Microsoft. Azure. Command. Automation. Model. CredentialInfo</span><span class="sxs-lookup"><span data-stu-id="cde5d-129">Microsoft.Azure.Commands.Automation.Model.CredentialInfo</span></span>

## <span data-ttu-id="cde5d-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="cde5d-130">NOTES</span></span>

## <span data-ttu-id="cde5d-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="cde5d-131">RELATED LINKS</span></span>

[<span data-ttu-id="cde5d-132">Get-AzureAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="cde5d-132">Get-AzureAutomationCredential</span></span>](./Get-AzureAutomationCredential.md)

[<span data-ttu-id="cde5d-133">Remove-AzureAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="cde5d-133">Remove-AzureAutomationCredential</span></span>](./Remove-AzureAutomationCredential.md)

[<span data-ttu-id="cde5d-134">Set-AzureAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="cde5d-134">Set-AzureAutomationCredential</span></span>](./Set-AzureAutomationCredential.md)


