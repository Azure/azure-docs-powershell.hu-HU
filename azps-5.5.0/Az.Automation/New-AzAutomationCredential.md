---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 739EB137-E4A8-4E85-96BD-4CF26D2C5763
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/new-azautomationcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationCredential.md
ms.openlocfilehash: a0b23cc5e16a723364d234eb2ee9723f291ee5e4
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100168306"
---
# <span data-ttu-id="57995-101">New-AzAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="57995-101">New-AzAutomationCredential</span></span>

## <span data-ttu-id="57995-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="57995-102">SYNOPSIS</span></span>
<span data-ttu-id="57995-103">Létrehoz egy automatizálási hitelesítő adatokat.</span><span class="sxs-lookup"><span data-stu-id="57995-103">Creates an Automation credential.</span></span>

## <span data-ttu-id="57995-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="57995-104">SYNTAX</span></span>

```
New-AzAutomationCredential [-Name] <String> [-Description <String>] [-Value] <PSCredential>
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="57995-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="57995-105">DESCRIPTION</span></span>
<span data-ttu-id="57995-106">A **New-AzAutomationCredential** parancsmag létrehoz egy hitelesítő adatokat **PSCredential** objektumként az Azure Automationben.</span><span class="sxs-lookup"><span data-stu-id="57995-106">The **New-AzAutomationCredential** cmdlet creates a credential as a **PSCredential** object in Azure Automation.</span></span>

## <span data-ttu-id="57995-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="57995-107">EXAMPLES</span></span>

### <span data-ttu-id="57995-108">1. példa: Hitelesítő adatok létrehozása</span><span class="sxs-lookup"><span data-stu-id="57995-108">Example 1: Create a credential</span></span>
```
PS C:\>$User = "Contoso\PFuller"
PS C:\> $Password = ConvertTo-SecureString "Password" -AsPlainText -Force
PS C:\> $Credential = New-Object -TypeName System.Management.Automation.PSCredential -ArgumentList $User, $Password
PS C:\> New-AzAutomationCredential -AutomationAccountName "Contoso17" -Name "ContosoCredential" -Value $Credential -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="57995-109">Az első parancs hozzárendel egy felhasználónevet a $User változóhoz.</span><span class="sxs-lookup"><span data-stu-id="57995-109">The first command assigns a user name to the $User variable.</span></span>
<span data-ttu-id="57995-110">A második parancs egy egyszerű szöveges jelszót biztonságos karakterláncsá alakít át a ConvertTo-SecureString parancsmag használatával.</span><span class="sxs-lookup"><span data-stu-id="57995-110">The second command converts a plain text password into a secure string by using the ConvertTo-SecureString cmdlet.</span></span>
<span data-ttu-id="57995-111">A parancs az objektumot a $Password tárolja.</span><span class="sxs-lookup"><span data-stu-id="57995-111">The command stores that object in the $Password variable.</span></span>
<span data-ttu-id="57995-112">A harmadik parancs létrehoz egy hitelesítő adatokat a $User és $Password alapján, majd tárolja azt a $Credential változóban.</span><span class="sxs-lookup"><span data-stu-id="57995-112">The third command creates a credential based on $User and $Password, and then stores it in the $Credential variable.</span></span>
<span data-ttu-id="57995-113">Az utolsó parancs létrehoz egy ContosoCredential nevű automatizálási hitelesítő adatokat, amely $Credential.</span><span class="sxs-lookup"><span data-stu-id="57995-113">The final command creates an Automation credential named ContosoCredential that uses $Credential.</span></span>

## <span data-ttu-id="57995-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="57995-114">PARAMETERS</span></span>

### <span data-ttu-id="57995-115">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="57995-115">-AutomationAccountName</span></span>
<span data-ttu-id="57995-116">Annak az automatizálási fióknak a nevét adja meg, amelyben ez a parancsmag tárolja a hitelesítő adatokat.</span><span class="sxs-lookup"><span data-stu-id="57995-116">Specifies the name of the Automation account in which this cmdlet stores the credential.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="57995-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="57995-117">-DefaultProfile</span></span>
<span data-ttu-id="57995-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="57995-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="57995-119">-Leírás</span><span class="sxs-lookup"><span data-stu-id="57995-119">-Description</span></span>
<span data-ttu-id="57995-120">Megadja a hitelesítő adatok leírását.</span><span class="sxs-lookup"><span data-stu-id="57995-120">Specifies a description for the credential.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="57995-121">-Name</span><span class="sxs-lookup"><span data-stu-id="57995-121">-Name</span></span>
<span data-ttu-id="57995-122">Megadja a hitelesítő adatok nevét.</span><span class="sxs-lookup"><span data-stu-id="57995-122">Specifies a name for the credential.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="57995-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="57995-123">-ResourceGroupName</span></span>
<span data-ttu-id="57995-124">Megadja annak az erőforráscsoportnak a leírását, amelyhez a parancsmag hitelesítő adatokat hoz létre.</span><span class="sxs-lookup"><span data-stu-id="57995-124">Specifies a description for the resource group for which this cmdlet creates a credential.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="57995-125">-Érték</span><span class="sxs-lookup"><span data-stu-id="57995-125">-Value</span></span>
<span data-ttu-id="57995-126">A hitelesítő adatokat **PSCredential** objektumként adja meg.</span><span class="sxs-lookup"><span data-stu-id="57995-126">Specifies the credentials as a **PSCredential** object.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="57995-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="57995-127">CommonParameters</span></span>
<span data-ttu-id="57995-128">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="57995-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="57995-129">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="57995-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="57995-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="57995-130">INPUTS</span></span>

### <span data-ttu-id="57995-131">System.String</span><span class="sxs-lookup"><span data-stu-id="57995-131">System.String</span></span>

### <span data-ttu-id="57995-132">System.Management.Automation.PSCredential</span><span class="sxs-lookup"><span data-stu-id="57995-132">System.Management.Automation.PSCredential</span></span>

## <span data-ttu-id="57995-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="57995-133">OUTPUTS</span></span>

### <span data-ttu-id="57995-134">Microsoft.Azure.Commands.Automation.Model.CredentialInfo</span><span class="sxs-lookup"><span data-stu-id="57995-134">Microsoft.Azure.Commands.Automation.Model.CredentialInfo</span></span>

## <span data-ttu-id="57995-135">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="57995-135">NOTES</span></span>

## <span data-ttu-id="57995-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="57995-136">RELATED LINKS</span></span>

[<span data-ttu-id="57995-137">Get-AzAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="57995-137">Get-AzAutomationCredential</span></span>](./Get-AzAutomationCredential.md)

[<span data-ttu-id="57995-138">Remove-AzAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="57995-138">Remove-AzAutomationCredential</span></span>](./Remove-AzAutomationCredential.md)

[<span data-ttu-id="57995-139">Set-AzAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="57995-139">Set-AzAutomationCredential</span></span>](./Set-AzAutomationCredential.md)


