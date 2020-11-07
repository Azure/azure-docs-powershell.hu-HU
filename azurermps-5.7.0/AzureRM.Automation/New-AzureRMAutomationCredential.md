---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 739EB137-E4A8-4E85-96BD-4CF26D2C5763
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/new-azurermautomationcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/New-AzureRMAutomationCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/New-AzureRMAutomationCredential.md
ms.openlocfilehash: 59a1b7bc849767f8d7d389631a69ae1fc93dc759
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93679901"
---
# <span data-ttu-id="448dc-101">New-AzureRmAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="448dc-101">New-AzureRmAutomationCredential</span></span>

## <span data-ttu-id="448dc-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="448dc-102">SYNOPSIS</span></span>
<span data-ttu-id="448dc-103">Automatizálási hitelesítő adatokat hoz létre.</span><span class="sxs-lookup"><span data-stu-id="448dc-103">Creates an Automation credential.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="448dc-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="448dc-104">SYNTAX</span></span>

```
New-AzureRmAutomationCredential [-Name] <String> [-Description <String>] [-Value] <PSCredential>
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="448dc-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="448dc-105">DESCRIPTION</span></span>
<span data-ttu-id="448dc-106">A **New-AzureRmAutomationCredential** parancsmag **PSCredential** -objektumként hozza létre a hitelesítő adatait az Azure automatizálásban.</span><span class="sxs-lookup"><span data-stu-id="448dc-106">The **New-AzureRmAutomationCredential** cmdlet creates a credential as a **PSCredential** object in Azure Automation.</span></span>

## <span data-ttu-id="448dc-107">Példák</span><span class="sxs-lookup"><span data-stu-id="448dc-107">EXAMPLES</span></span>

### <span data-ttu-id="448dc-108">Példa 1: hitelesítő adatok létrehozása</span><span class="sxs-lookup"><span data-stu-id="448dc-108">Example 1: Create a credential</span></span>
```
PS C:\>$User = "Contoso\PFuller"
PS C:\> $Password = ConvertTo-SecureString "Password" -AsPlainText -Force
PS C:\> $Credential = New-Object -TypeName System.Management.Automation.PSCredential -ArgumentList $User, $Password
PS C:\> New-AzureRmAutomationCredential -AutomationAccountName "Contoso17" -Name "ContosoCredential" -Value $Credential -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="448dc-109">Az első parancs a felhasználónevet hozzárendeli a $User változóhoz.</span><span class="sxs-lookup"><span data-stu-id="448dc-109">The first command assigns a user name to the $User variable.</span></span>

<span data-ttu-id="448dc-110">A második parancs az egyszerű szöveges jelszót egy biztonságos karakterláncba konvertálja a ConvertTo-SecureString parancsmag használatával.</span><span class="sxs-lookup"><span data-stu-id="448dc-110">The second command converts a plain text password into a secure string by using the ConvertTo-SecureString cmdlet.</span></span>
<span data-ttu-id="448dc-111">A parancs az objektumot a $Password változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="448dc-111">The command stores that object in the $Password variable.</span></span>

<span data-ttu-id="448dc-112">A harmadik parancs a hitelesítő adatokat $User és a $Password alapján hozza létre, majd a $Credential változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="448dc-112">The third command creates a credential based on $User and $Password, and then stores it in the $Credential variable.</span></span>

<span data-ttu-id="448dc-113">A végleges parancs létrehoz egy ContosoCredential nevű automatizálási hitelesítő adatokat, amely a $Credentialt használja.</span><span class="sxs-lookup"><span data-stu-id="448dc-113">The final command creates an Automation credential named ContosoCredential that uses $Credential.</span></span>

## <span data-ttu-id="448dc-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="448dc-114">PARAMETERS</span></span>

### <span data-ttu-id="448dc-115">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="448dc-115">-AutomationAccountName</span></span>
<span data-ttu-id="448dc-116">Annak az automatizálási fióknak a nevét adja meg, amelyben a parancsmag a hitelesítő adatokat tárolja.</span><span class="sxs-lookup"><span data-stu-id="448dc-116">Specifies the name of the Automation account in which this cmdlet stores the credential.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="448dc-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="448dc-117">-DefaultProfile</span></span>
<span data-ttu-id="448dc-118">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="448dc-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="448dc-119">-Leírás</span><span class="sxs-lookup"><span data-stu-id="448dc-119">-Description</span></span>
<span data-ttu-id="448dc-120">A hitelesítő adatok leírását adja meg.</span><span class="sxs-lookup"><span data-stu-id="448dc-120">Specifies a description for the credential.</span></span>

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

### <span data-ttu-id="448dc-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="448dc-121">-Name</span></span>
<span data-ttu-id="448dc-122">A hitelesítő adatok nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="448dc-122">Specifies a name for the credential.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="448dc-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="448dc-123">-ResourceGroupName</span></span>
<span data-ttu-id="448dc-124">Annak az erőforráscsoportnak a leírását adja meg, amelyhez a parancsmag hitelesítő adatokat hoz létre.</span><span class="sxs-lookup"><span data-stu-id="448dc-124">Specifies a description for the resource group for which this cmdlet creates a credential.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="448dc-125">-Value (érték)</span><span class="sxs-lookup"><span data-stu-id="448dc-125">-Value</span></span>
<span data-ttu-id="448dc-126">A hitelesítő adatokat **PSCredential** -objektumként adja meg.</span><span class="sxs-lookup"><span data-stu-id="448dc-126">Specifies the credentials as a **PSCredential** object.</span></span>

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="448dc-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="448dc-127">CommonParameters</span></span>
<span data-ttu-id="448dc-128">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="448dc-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="448dc-129">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="448dc-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="448dc-130">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="448dc-130">INPUTS</span></span>

### <span data-ttu-id="448dc-131">Nincs</span><span class="sxs-lookup"><span data-stu-id="448dc-131">None</span></span>
<span data-ttu-id="448dc-132">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="448dc-132">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="448dc-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="448dc-133">OUTPUTS</span></span>

### <span data-ttu-id="448dc-134">Microsoft. Azure. Command. Automation. Model. CredentialInfo</span><span class="sxs-lookup"><span data-stu-id="448dc-134">Microsoft.Azure.Commands.Automation.Model.CredentialInfo</span></span>

## <span data-ttu-id="448dc-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="448dc-135">NOTES</span></span>

## <span data-ttu-id="448dc-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="448dc-136">RELATED LINKS</span></span>

[<span data-ttu-id="448dc-137">Get-AzureRmAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="448dc-137">Get-AzureRmAutomationCredential</span></span>](./Get-AzureRMAutomationCredential.md)

[<span data-ttu-id="448dc-138">Remove-AzureRmAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="448dc-138">Remove-AzureRmAutomationCredential</span></span>](./Remove-AzureRMAutomationCredential.md)

[<span data-ttu-id="448dc-139">Set-AzureRmAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="448dc-139">Set-AzureRmAutomationCredential</span></span>](./Set-AzureRMAutomationCredential.md)


