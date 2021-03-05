---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 739EB137-E4A8-4E85-96BD-4CF26D2C5763
online version: https://docs.microsoft.com/powershell/module/az.automation/new-azautomationcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationCredential.md
ms.openlocfilehash: 9858bfdd4aa8388d7e5afa0d2f3ee660bef3a166
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102012742"
---
# <span data-ttu-id="79ad6-101">New-AzAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="79ad6-101">New-AzAutomationCredential</span></span>

## <span data-ttu-id="79ad6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="79ad6-102">SYNOPSIS</span></span>
<span data-ttu-id="79ad6-103">Létrehoz egy automatizálási hitelesítő adatokat.</span><span class="sxs-lookup"><span data-stu-id="79ad6-103">Creates an Automation credential.</span></span>

## <span data-ttu-id="79ad6-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="79ad6-104">SYNTAX</span></span>

```
New-AzAutomationCredential [-Name] <String> [-Description <String>] [-Value] <PSCredential>
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="79ad6-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="79ad6-105">DESCRIPTION</span></span>
<span data-ttu-id="79ad6-106">A **New-AzAutomationCredential** parancsmag **PSCredential** objektumként hoz létre hitelesítő adatokat az Azure Automationben.</span><span class="sxs-lookup"><span data-stu-id="79ad6-106">The **New-AzAutomationCredential** cmdlet creates a credential as a **PSCredential** object in Azure Automation.</span></span>

## <span data-ttu-id="79ad6-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="79ad6-107">EXAMPLES</span></span>

### <span data-ttu-id="79ad6-108">1. példa: Hitelesítő adatok létrehozása</span><span class="sxs-lookup"><span data-stu-id="79ad6-108">Example 1: Create a credential</span></span>
```
PS C:\>$User = "Contoso\PFuller"
PS C:\> $Password = ConvertTo-SecureString "Password" -AsPlainText -Force
PS C:\> $Credential = New-Object -TypeName System.Management.Automation.PSCredential -ArgumentList $User, $Password
PS C:\> New-AzAutomationCredential -AutomationAccountName "Contoso17" -Name "ContosoCredential" -Value $Credential -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="79ad6-109">Az első parancs hozzárendel egy felhasználónevet a $User változóhoz.</span><span class="sxs-lookup"><span data-stu-id="79ad6-109">The first command assigns a user name to the $User variable.</span></span>
<span data-ttu-id="79ad6-110">A második parancs egy egyszerű szöveges jelszót biztonságos karakterláncsá alakít át a ConvertTo-SecureString parancsmag használatával.</span><span class="sxs-lookup"><span data-stu-id="79ad6-110">The second command converts a plain text password into a secure string by using the ConvertTo-SecureString cmdlet.</span></span>
<span data-ttu-id="79ad6-111">A parancs az objektumot a $Password tárolja.</span><span class="sxs-lookup"><span data-stu-id="79ad6-111">The command stores that object in the $Password variable.</span></span>
<span data-ttu-id="79ad6-112">A harmadik parancs létrehoz egy hitelesítő adatokat a $User és $Password alapján, majd tárolja azt a $Credential változóban.</span><span class="sxs-lookup"><span data-stu-id="79ad6-112">The third command creates a credential based on $User and $Password, and then stores it in the $Credential variable.</span></span>
<span data-ttu-id="79ad6-113">Az utolsó parancs létrehoz egy ContosoCredential nevű automatizálási hitelesítő adatokat, amely a $Credential.</span><span class="sxs-lookup"><span data-stu-id="79ad6-113">The final command creates an Automation credential named ContosoCredential that uses $Credential.</span></span>

## <span data-ttu-id="79ad6-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="79ad6-114">PARAMETERS</span></span>

### <span data-ttu-id="79ad6-115">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="79ad6-115">-AutomationAccountName</span></span>
<span data-ttu-id="79ad6-116">Annak az automatizálási fióknak a nevét adja meg, amelyben ez a parancsmag tárolja a hitelesítő adatokat.</span><span class="sxs-lookup"><span data-stu-id="79ad6-116">Specifies the name of the Automation account in which this cmdlet stores the credential.</span></span>

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

### <span data-ttu-id="79ad6-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="79ad6-117">-DefaultProfile</span></span>
<span data-ttu-id="79ad6-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="79ad6-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="79ad6-119">-Leírás</span><span class="sxs-lookup"><span data-stu-id="79ad6-119">-Description</span></span>
<span data-ttu-id="79ad6-120">Megadja a hitelesítő adatok leírását.</span><span class="sxs-lookup"><span data-stu-id="79ad6-120">Specifies a description for the credential.</span></span>

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

### <span data-ttu-id="79ad6-121">-Name</span><span class="sxs-lookup"><span data-stu-id="79ad6-121">-Name</span></span>
<span data-ttu-id="79ad6-122">Megadja a hitelesítő adatok nevét.</span><span class="sxs-lookup"><span data-stu-id="79ad6-122">Specifies a name for the credential.</span></span>

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

### <span data-ttu-id="79ad6-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="79ad6-123">-ResourceGroupName</span></span>
<span data-ttu-id="79ad6-124">Megadja annak az erőforráscsoportnak a leírását, amelyhez a parancsmag hitelesítő adatokat hoz létre.</span><span class="sxs-lookup"><span data-stu-id="79ad6-124">Specifies a description for the resource group for which this cmdlet creates a credential.</span></span>

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

### <span data-ttu-id="79ad6-125">-Érték</span><span class="sxs-lookup"><span data-stu-id="79ad6-125">-Value</span></span>
<span data-ttu-id="79ad6-126">A hitelesítő adatokat **PSCredential** objektumként adja meg.</span><span class="sxs-lookup"><span data-stu-id="79ad6-126">Specifies the credentials as a **PSCredential** object.</span></span>

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

### <span data-ttu-id="79ad6-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="79ad6-127">CommonParameters</span></span>
<span data-ttu-id="79ad6-128">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="79ad6-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="79ad6-129">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="79ad6-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="79ad6-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="79ad6-130">INPUTS</span></span>

### <span data-ttu-id="79ad6-131">System.String</span><span class="sxs-lookup"><span data-stu-id="79ad6-131">System.String</span></span>

### <span data-ttu-id="79ad6-132">System.Management.Automation.PSCredential</span><span class="sxs-lookup"><span data-stu-id="79ad6-132">System.Management.Automation.PSCredential</span></span>

## <span data-ttu-id="79ad6-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="79ad6-133">OUTPUTS</span></span>

### <span data-ttu-id="79ad6-134">Microsoft.Azure.Commands.Automation.Model.CredentialInfo</span><span class="sxs-lookup"><span data-stu-id="79ad6-134">Microsoft.Azure.Commands.Automation.Model.CredentialInfo</span></span>

## <span data-ttu-id="79ad6-135">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="79ad6-135">NOTES</span></span>

## <span data-ttu-id="79ad6-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="79ad6-136">RELATED LINKS</span></span>

[<span data-ttu-id="79ad6-137">Get-AzAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="79ad6-137">Get-AzAutomationCredential</span></span>](./Get-AzAutomationCredential.md)

[<span data-ttu-id="79ad6-138">Remove-AzAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="79ad6-138">Remove-AzAutomationCredential</span></span>](./Remove-AzAutomationCredential.md)

[<span data-ttu-id="79ad6-139">Set-AzAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="79ad6-139">Set-AzAutomationCredential</span></span>](./Set-AzAutomationCredential.md)


